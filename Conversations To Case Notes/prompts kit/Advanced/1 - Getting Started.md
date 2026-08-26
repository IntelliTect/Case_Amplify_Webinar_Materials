# Advanced — Getting Started

**For whoever manages your AI workspace, writes automations, or builds shared assistants for a team.**

---

## What this path is

The same documentation behavior as the Starter and Standard paths, packaged as reusable configuration rather than text a person pastes. Three deliverables:

| File | What it is | Use it when |
|---|---|---|
| **2 - Reusable Instruction File** | A portable instruction file with the guardrails and all five task recipes in one document | You want one artifact that travels between tools, or drives an AI assistant that loads instructions from a file |
| **3 - API System Prompt** | The instructions as a system prompt, with the request pattern | You're calling a model programmatically — a script, an integration, a scheduled job |
| **4 - Custom Assistant Configuration** | Field-by-field setup for a shared custom assistant | You want one assistant your whole team uses, without each person configuring their own |

---

## Non-technical readers welcome

If you're not the person who writes code, you can still read this folder usefully — it tells you what your technical colleague is setting up and what to ask them about. The three questions worth asking are all in the compliance section below, and none of them require you to read a line of code.

If you're here because someone forwarded you this folder and asked "can we do this?" — the answer is yes, and the constraint that matters is at the top of the next section.

---

## The non-negotiable part

**Everything in this folder must run against a covered endpoint or workspace, with training off and retention minimized.** That is a harder requirement than in the other two paths, for a reason worth understanding: automation removes the human pause. A caseworker pasting into a chat window notices when something looks wrong. A scheduled job processing two hundred transcripts overnight does not.

Three things to confirm before any real client data flows:

1. **A signed BAA or DPA is in place** covering the specific endpoint or workspace you're using, on the specific plan.
2. **Training on your inputs is off** — ideally by contract, not just by setting.
3. **Retention is set to zero or the practical minimum**, and you know where the data is processed.

### The mistake to avoid, by platform

- **Claude:** the Enterprise plan or the Anthropic API. Not Free, Pro, Max, or Team.
- **OpenAI:** Enterprise, Edu, Healthcare, or the API. Not Free, Plus, Pro, or Business.
- **Google — read this one carefully.** The **Gemini API on Google AI Studio is not covered, on either the free or the paid tier.** Google says so directly: *"No compliance certifications (for example, HIPAA, SOC2). Regulated customers should use Vertex AI instead."* The covered path is **Gemini Enterprise Agent Platform** (formerly Vertex AI) under a Google Cloud agreement. Same models, different door — and paying for API quota buys you no-training terms, not an agreement. This is the single most common misstep on the Google side.
- **Azure OpenAI:** text endpoints are covered under Microsoft's agreement. **Realtime audio is not** — it remains outside HIPAA scope. Don't route voice through it.
- **Anywhere on Google Cloud:** pre-release and preview features are excluded from use with protected information unless the terms expressly say otherwise.

### The gap people miss entirely

**Logging.** If your application sends prompts or responses to a third-party logging, monitoring, or analytics service, that service is now handling protected information — and it needs to be covered by your agreement too. Most aren't, and nobody notices because logging is infrastructure rather than a feature.

Keep request and response logging off, or keep it inside your own boundary. If you need observability, log metadata and identifiers rather than content.

---

## What stays the same as the other paths

**A human reviews and signs off before anything enters the record.** Automation makes drafting cheap; it does not make review optional. If you're building a pipeline, build the review step into it as a required state — not as a convention people are expected to follow.

Every task output still ends with the Review & Sign-off block. Don't strip it because it's awkward to parse. It's the part that keeps the AI's work labeled as a draft.

---

## Suggested order

Read **2 - Reusable Instruction File** first — it's the canonical version of the behavior, and files 3 and 4 both reference it. Then whichever of 3 or 4 matches what you're building.

The prompt text is identical across all three paths, so if you want to see how a task behaves in isolation before wiring it up, the files in **Starter** are the fastest way to test it by hand.
