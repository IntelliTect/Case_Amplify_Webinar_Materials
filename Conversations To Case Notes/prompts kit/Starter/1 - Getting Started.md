# Starter — Getting Started

**Read this first. It takes about three minutes, and then you can use everything else in this folder.**

---

## What this path is

The Starter path is copy and paste. There is nothing to install, configure, or save. You open your organization's approved AI tool, paste some text into the chat box, and read what comes back.

That's it. Many people never need anything more.

---

## Try it on invented data first

Before you use any of this on a real client conversation, run it once on the fictional one in
**9 - Sample Conversation**. Every worked example in this folder uses it, so you can compare
what you get to what's shown and see where AI output needs a human. It takes about ten minutes
and it is the fastest way to build a feel for what to check.

---

## Before your first try — one check

Client information may only go into an AI tool your organization has under a **signed agreement** — a BAA if you handle protected health information, or a DPA otherwise.

**If you don't know whether your tool is covered, ask before you paste anything real.** Whoever manages your organization's software will know. While you're waiting, you can practice on the fictional example in each file.

Two specific things to avoid:

- **The free version of a paid product is usually not covered.** Same logo, different rules.
- **If you use Gemini, don't use Gemini in Chrome or Gemini Notebook** for client information. Both are excluded from Google's agreement even when the rest of your Workspace subscription is covered.

---

## The running order

Every task works the same way. Three steps in, one step after.

**Step 1 — Set the AI up.** Open a new chat and paste in the **Master Instructions** (file 2). Send it. This tells the AI that it's a documentation assistant, how to write, and what it must never do. This is the single most important piece — the other prompts assume it's already there.

**Step 2 — Give it the conversation.** Paste your transcript or notes. Send it.

**Step 3 — Ask for one task.** Paste one prompt from this folder. Send it.

**Step 4 — Review and sign.** Read what came back. Fix what's wrong. Only then does it go anywhere near the record.

> **One exception:** if you're only removing identifying details (file 7), you don't need the Master Instructions first. Just paste the text and the prompt.

---

## Which file do I want?

| I want to… | Use |
|---|---|
| Set the AI up (do this first) | **2 - Master Instructions** |
| Turn a long conversation into a short summary | **3 - Summarize Prompt** |
| Pull the facts into a spreadsheet | **4 - Extract Data Prompt** |
| Get a to-do list with owners and deadlines | **5 - Organize Action Items Prompt** |
| Write a case note | **6 - Draft Case Note Prompt** |
| Strip out names, dates, and numbers | **7 - De-Identify Prompt** |
| See the different case note formats | **8 - Case Note Format Templates** |
| Practise on invented data before using real client information | **9 - Sample Conversation** |

---

## Where to paste — by tool

### Claude

1. Sign in to your organization's **Claude Enterprise** workspace, or use the Anthropic API. **Not** Free, Pro, Max, or Team — none of those can be covered.
2. Start a **New chat**.
3. Paste the Master Instructions → Send.
4. Paste the conversation → Send.
5. Paste one task prompt → Send.

### ChatGPT

1. Sign in to **ChatGPT Enterprise, Edu, or ChatGPT for Healthcare**, or use the OpenAI API. **Not** Free, Plus, Pro, or Business — Business cannot be covered.
2. Start a **New chat**.
3. Paste the Master Instructions → Send.
4. Paste the conversation → Send.
5. Paste one task prompt → Send.

### Gemini

1. Sign in to your organization's **Google Workspace** account — the one where an administrator has accepted the agreement and Gemini is turned on as a **Core Service**. **Not** a personal Google account, and not Google AI Pro or Ultra.
2. Go to **gemini.google.com**, or click **Ask Gemini** in the side panel of Gmail, Docs, Drive, or Sheets.
3. Start a **new chat**.
4. Paste the Master Instructions → Send.
5. Paste the conversation → Send.
6. Paste one task prompt → Send.

> **Gemini note:** your Gemini activity history is on by default and only an administrator can turn it off. They also set how long it's kept — 3, 18, or 36 months. Worth asking what yours is set to.

---

## Two habits that matter more than any prompt

**Send only what the task needs.** A summary needs the story, not the Social Security number. You don't have to paste everything just because you have it. The one exception is pulling identifiers into fields — that task needs them, which is exactly why it may only happen in a covered tool.

**Never let the AI have the last word.** Every prompt in this folder ends its output with a Review & Sign-off block: what it assumed, what a human should check, and a line for your name. That block is not decoration. Read it first, then read the output against it.

---

## When something looks wrong

| What you see | What's happening | What to do |
|---|---|---|
| Chatty, complimentary tone ("productive meeting!") | The Master Instructions aren't loaded, or the chat got too long and pushed them out | Paste the Master Instructions again, or start a fresh chat |
| A fact you don't recognize | The AI filled a gap instead of leaving it blank | Don't fix it in the output — fix the prompt by re-running, and report it. Guessing is a failure, not a quirk |
| An identifier in an output that didn't need it | Minimum-necessary slipped | Remove it, and check whether you needed to paste it at all |
| No Review & Sign-off block | The instructions weren't followed | Re-run with the Master Instructions loaded first |

---

## Ready for the next step?

If you find yourself pasting the Master Instructions over and over, move to the **Standard** folder. It shows you how to save them once so every new conversation already knows what to do. Ten minutes, one time.
