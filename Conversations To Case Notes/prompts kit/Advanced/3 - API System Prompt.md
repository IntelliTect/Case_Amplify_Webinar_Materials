# API System Prompt

For calling a model directly from code — a script, an integration, a scheduled job.

**The pattern.** The Master Instructions become the **system prompt**. The transcript plus one task instruction becomes the **user message**. Works the same way against the Anthropic Messages API, the OpenAI Chat Completions API, or Google's models on a covered Google Cloud endpoint.

---

## ⚠️ Before you send a single real transcript

Confirm all three:

1. **A signed BAA or DPA is in place** covering this specific endpoint and plan.
2. **Training on your inputs is off.**
3. **Retention is zero or minimized**, and you know where processing happens.

**Google's API path is the one that trips people up.** The **Gemini API on Google AI Studio is not covered on either the free or the paid tier** — Google's own words: *"No compliance certifications (for example, HIPAA, SOC2). Regulated customers should use Vertex AI instead."* The covered path is **Gemini Enterprise Agent Platform** (formerly Vertex AI) under a Google Cloud agreement. Paying for API quota buys no-training terms, not an agreement.

**Azure OpenAI:** text endpoints are covered under Microsoft's agreement; **Realtime audio is not.** Don't route voice through it.

---

## The shape of a request

```
system:  <the full Master Instructions — see Starter / 2 - Master Instructions>

user:    TASK: Summarize this conversation for the case file using the sections
         Contact & Context; Presenting Needs; Key Facts; Actions Taken & Next
         Steps. Report only what was stated.

         TRANSCRIPT:
         <the transcript text>
```

Swap the `TASK:` line to change the job. The system prompt stays constant.

| Task | The TASK line |
|---|---|
| Summarize | The four sections, as above |
| Extract | Ask for the three labeled CSV blocks (see *Starter / 4 - Extract Data Prompt*) |
| Organize | Action items table, referrals, deadline timeline |
| Draft a note | Include a `FORMAT:` line — General-purpose, SOAP, DAP, GIRP, or Case Amplify |
| De-identify | The 18-category replacement list (see *Starter / 7 - De-Identify Prompt*) |

---

## Four things to get right in the implementation

**Don't log the content.** This is the failure nobody notices, because logging is infrastructure rather than a feature. If your application ships prompts or responses to a third-party logging, monitoring, error-tracking, or analytics service, that service is now handling protected information and needs to be covered by your agreement too. Most aren't.

Keep request and response logging off, or keep it inside your own boundary. Log identifiers, timings, token counts, and error codes — not content. If you need to debug a bad output, reproduce it in a covered interactive session rather than reading it out of a log.

**Practice minimum-necessary at the API layer too.** The same rule that applies to a caseworker pasting into a chat window applies to your code. If the task is a summary, don't send the identifier fields just because your data layer returned them. Build the trimming into the request, not into a reviewer's hopes.

**Enforce the extract restriction at the endpoint, not in the prompt.** The extract task captures identifiers, so it can only run against a covered endpoint. An instruction telling a model not to do something is a suggestion; a configuration that makes the uncovered endpoint unreachable for that code path is a control. Build the control.

**Keep the Review & Sign-off block, and make review a required state.** Parse around the block if you must, but don't remove it from the output, and don't let a record be created from an unreviewed draft. If your pipeline writes to a case system, the AI's output should land somewhere that requires a human action before it becomes part of the record — a draft state, a review queue, an approval flag. Automation makes drafting cheap and makes skipping review easy. Design against that.

---

## On determinism and drift

Model behavior changes when the model version changes, and the change is usually an improvement that nonetheless breaks a downstream parser. Two practical habits:

**Pin the model version** rather than tracking a moving alias, and re-test when you upgrade.

**Validate the shape before you trust it.** The extract task in particular emits CSV that something downstream will parse. Check that the blocks are present and the columns match before writing anything anywhere. A malformed extract that silently half-imports is worse than one that fails loudly.

One provider-specific note worth knowing: Anthropic's newest models require 30-day retention and cannot run with zero-data-retention enabled. If your compliance posture requires zero retention, that constrains which models you can use — so "always use the newest model" and "always use zero retention" can be in genuine conflict. Decide deliberately rather than discovering it during an audit.
