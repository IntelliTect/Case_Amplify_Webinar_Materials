# AI Prompts Kit for Case Management

A ready-to-use set of instructions and prompts for turning a client conversation into clean, accurate case documentation — a summary, structured data, action items, and a draft case note — using AI tools your organization already has.

Everything here is written to be copied and pasted. You do not need any technical skill to use the Starter path.

---

## The one rule that governs all of it

> **Send the AI only what the task actually needs — and nothing more. Do it in a tool your organization has under a signed agreement. A human reviews and signs off before anything enters the record.**

If you remember nothing else from this kit, remember that sentence.

---

## Before you use any of this: is your tool covered?

Client information may only go into an AI tool your organization has under a **signed agreement**:

- A **BAA** (Business Associate Agreement) if you handle protected health information.
- A **DPA** (Data Processing Agreement) if you are not HIPAA-covered but still handle sensitive client data.

**Paying for a tool is not the same as being covered.** The plan matters as much as the product:

| Tool | Covered plans | **Not** covered |
|---|---|---|
| **Claude** (Anthropic) | Enterprise plan, or the Anthropic API | Free, Pro, Max, **Team** |
| **ChatGPT** (OpenAI) | Enterprise, Edu, ChatGPT for Healthcare, or the OpenAI API | Free, Plus, Pro, **Business** |
| **Gemini** (Google) | Any paid Google Workspace edition once an administrator accepts the agreement, or Google Cloud | The consumer Gemini app (Free, AI Plus, AI Pro, AI Ultra), the Gemini API on Google AI Studio (free *and* paid), **Gemini in Chrome**, **Gemini Notebook** |

A few traps worth knowing:

- **Same logo, different rules.** The free version of a product your organization pays for is usually not covered.
- **Gemini is covered by *edition*, not by price** — but four Gemini surfaces are excluded even on a covered subscription. Gemini Notebook is the dangerous one, because it holds uploaded documents and it's exactly where someone would put a transcript.
- **"We're HIPAA compliant" on a website is not an agreement.** That phrase describes a vendor's internal security practices. Ask for the signed BAA or DPA.

*Plan and coverage details were verified in August 2026. Vendor terms change — confirm with whoever manages your organization's software before you rely on any of this.*

---

## Three paths — pick the one that fits you

You do not need to work through all three. Each path is complete on its own.

### 🟢 Starter — copy and paste
**For everyone. No setup at all.**

You open your organization's approved AI tool, paste in some text, and go. Every prompt is plain text you can copy. This is where almost everyone should begin, and many people never need to go further.

**Time to first result:** about five minutes.
**Folder:** `Starter/` — start with *1 - Getting Started*.

### 🔵 Standard — set it up once
**For people comfortable clicking around their AI tool's settings.**

Instead of pasting the instructions into every new conversation, you save them once. Then every new chat already knows the role, the format, and the rules. You still paste the client conversation and pick a task, but the setup is done.

**Time to set up:** about ten minutes, once.
**Folder:** `Standard/` — start with *1 - Getting Started*.

### 🟣 Advanced — build it into your tools
**For whoever manages your AI workspace, writes automations, or builds shared assistants.**

The same behavior, packaged as reusable configuration: a portable instruction file, a system prompt for direct programming access, and a shared custom assistant your whole team can use.

**Folder:** `Advanced/` — start with *1 - Getting Started*.

> **A note for technical readers:** the Starter and Standard folders are written for a non-technical audience on purpose, but the prompt text itself is the same across all three paths. If you are implementing this, read `Advanced/1 - Getting Started` first, then lift the prompt bodies from the Starter files.

---

## What's in each path

| | Starter | Standard | Advanced |
|---|---|---|---|
| Instructions that set the AI up | Paste each time | **Saved once** | Packaged as a file or system prompt |
| Summarize a conversation | ✅ | ✅ | ✅ |
| Extract data into a spreadsheet | ✅ | ✅ | ✅ |
| Organize action items and deadlines | ✅ | ✅ | ✅ |
| Draft a case note (5 formats) | ✅ | ✅ | ✅ |
| Remove identifying details | ✅ | ✅ | ✅ |
| Sample conversation to practise on | ✅ | ✅ | ✅ |
| Shared across your team | — | Sometimes | ✅ |

---

## How the pieces fit together

Every task follows the same three steps:

1. **Set up the AI** — give it the Master Instructions, so it knows it's a documentation assistant and not a chatbot.
2. **Give it the conversation** — paste the transcript or notes.
3. **Ask for one task** — summarize, extract, organize, draft a note, or remove identifying details.

Then you do the fourth step, which is the one that matters most: **you read it, correct it, and sign it.** Every output ends with a Review & Sign-off block for exactly that reason. The AI drafts. You decide.

---

## About the examples

Every prompt file includes a worked example so you can see what good output actually looks like before you try it on real work. The examples all use the same fictional client conversation — a benefits recertification check-in with a client named Marisol Reyes. **Every name, date, and number in those examples is invented.**

**That conversation is included**, in `Starter/9 - Sample Conversation`, along with an answer key. Run any prompt against it, compare your result to the worked example, and you'll see where AI output needs a human before you use it on a real case. Practising there rather than on a live file is also the safe way to test whether your organization's tool behaves the way you expect.

---

## What this kit is not

- It is **not** legal or compliance advice. Have your compliance officer or counsel review anything here before it becomes organizational policy.
- It does **not** replace your program's documentation standards. Where a format here conflicts with what your funder or program requires, your program wins.
- It does **not** make a decision for you. No output from these prompts belongs in a client record until a person has read it and signed off.
