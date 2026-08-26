# Standard — Getting Started

**For people comfortable clicking around their AI tool's settings. About ten minutes, once.**

---

## What this path is, and why bother

In the Starter path you paste the Master Instructions at the top of every new conversation. That works, but it gets old — and it fails quietly in a way worth knowing about: in a long conversation, the instructions can drift out of the AI's view, and the output slowly gets chattier and less careful without anyone noticing.

The Standard path fixes both. You save the instructions **once**, into a saved workspace your AI tool provides. Every new conversation you start there already knows the role, the format, the tone, and the guardrails.

You still paste the client conversation and pick a task. You've just stopped re-pasting the setup.

---

## What you're setting up

Each of the three tools has its own name for the same idea — a saved container that holds standing instructions:

| Tool | What it's called | Where |
|---|---|---|
| **Claude** | a **Project** | Projects → Create Project |
| **ChatGPT** | a **Project** | Sidebar → + → Project |
| **Gemini** | a **Gem** | Sidebar → Gems → New Gem |

Pick the file for your tool:

- **2 - Set Up in Claude (Projects)**
- **3 - Set Up in ChatGPT (Projects)**
- **4 - Set Up in Gemini (Gems)**

You only need the one your organization uses.

---

## The one rule that doesn't change

**Your saved workspace must live in the account your organization has under a signed BAA or DPA.**

This matters more here than in the Starter path, because a saved workspace is persistent. A conversation you paste into and close is a moment. A Project or Gem is a place that accumulates — instructions, attached files, and every conversation held inside it. If it's in the wrong account, the exposure doesn't end when you close the tab.

Two specific cautions:

- **Don't recreate your work setup in a personal account** because it's more convenient. Same product, same interface, no agreement.
- **Attach templates, not clients.** Adding the case note templates as a reference file is fine. Uploading real client files is still protected information and belongs only in the covered workspace — and for Gemini specifically, read the storage caution in file 4 before attaching anything.

---

## What this does *not* do

**It saves the instructions. It does not save the review step.**

A human still reads, corrects, and signs off on every output before it enters the record. Saving the setup makes the drafting faster; it doesn't make the draft trustworthy. The Review & Sign-off block still appears at the end of every response, and it still needs a person.

---

## After you've set it up

Your daily use becomes two steps instead of three:

1. Open a new conversation **inside** your Project or Gem.
2. Paste the client conversation, then paste one task prompt.

The task prompts themselves are unchanged — use the files in the **Starter** folder:

- *3 - Summarize Prompt*
- *4 - Extract Data Prompt*
- *5 - Organize Action Items Prompt*
- *6 - Draft Case Note Prompt*
- *7 - De-Identify Prompt*

Keep the Starter folder. This path replaces the setup step, not the prompts.

---

## How to tell it's working

Start a conversation in your new Project or Gem, paste any short piece of text, and ask it to summarize for the case file. You should get back neutral, sectioned output ending in a Review & Sign-off block — **without** having pasted any instructions.

If you get a chatty, complimentary paragraph with no review block, the instructions didn't save. Go back and check they're in the instructions field and that you clicked Save.
