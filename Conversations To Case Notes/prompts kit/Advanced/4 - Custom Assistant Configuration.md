# Custom Assistant Configuration

One shared assistant your whole team uses, instead of each person configuring their own. Written for a **Custom GPT** in a ChatGPT Enterprise, Edu, or Healthcare workspace; the same fields map closely onto equivalent features in other tools.

---

## ⚠️ Build it in a covered workspace only

A custom assistant runs under **the builder's** account and data controls, not the user's. So whoever creates it determines whether every conversation held with it is covered.

Build only in **ChatGPT Enterprise, Edu, or ChatGPT for Healthcare**. **Never in Business or a personal plan** — OpenAI does not offer an agreement for ChatGPT Business, and an assistant built there is uncovered no matter who uses it or how careful they are.

---

## Configuration

| Field | Value |
|---|---|
| **Name** | Case Documentation Assistant |
| **Description** | Objective case documentation from a client conversation — summary, CSV extract, action items, de-identification, and draft notes. Human review required. |
| **Instructions** | Paste the **Master Instructions** (*Starter / 2 - Master Instructions*), then append the five task recipes from *2 - Reusable Instruction File* so the assistant knows each job's exact format. |
| **Conversation starters** | "Summarize this conversation for the case file" · "Extract the key info as CSV (3 blocks)" · "Organize this into action items, referrals, and a deadline timeline" · "Draft a case note — format: SOAP" · "De-identify this text (HIPAA Safe Harbor)" |
| **Knowledge** | *Optional:* upload *Starter / 8 - Case Note Format Templates*. **Nothing else.** See the caution below. |
| **Capabilities** | Turn **OFF** web browsing, image generation, and code interpreter. |

---

## Why turn the capabilities off

Not caution for its own sake — each one is a specific hole.

**Web browsing** sends content out to a search provider and to whatever pages it fetches. Those are not covered by your agreement. A model deciding on its own that a client's situation warrants looking something up is a disclosure you didn't authorize and won't see.

**Code interpreter** executes in a sandbox that receives whatever data it's given, adding a processing surface with its own retention behavior for no benefit to any task in this kit.

**Image generation** has no use here at all.

Fewer moving parts, tighter minimum-necessary, and no data leaving through features nobody is using.

---

## The knowledge-file caution

Anything uploaded as knowledge **lives in the workspace and is readable by everyone who can use the assistant.** Templates are fine. Real client files are not — an uploaded transcript becomes visible to every user of the assistant, which is almost never what the uploader intended.

Say this explicitly when you roll the assistant out. "Don't upload client files to the assistant" is not obvious to someone who has just been shown how helpful uploading a file is.

---

## Sharing

**Share only inside the covered workspace.** A custom assistant is not a way to move protected information outside your covered environment, and sharing it more widely doesn't extend your agreement — it just widens who can send data into it.

**Actions need their own review.** If you connect the assistant to an external API, that connection touches protected information and requires its own compliance review before it goes anywhere near real client data. An assistant that can write to an outside system is a data-transfer pathway, whatever it's called in the interface.

---

## Rolling it out to a team

The configuration is the easy part. Three things determine whether this actually helps:

**Tell people what it is *not*.** The assistant drafts. It does not decide, and nothing it produces is a record until a person signs off. If the first thing your team learns is how fast it is, the second thing they'll learn is how easy it is to paste the output straight into a case file. Lead with the review step.

**Point them at the Starter folder anyway.** The assistant makes the tasks convenient; the Starter files explain what to check in each output. Convenience without the checking guidance produces confident, unexamined documentation — worse than what people were doing before.

**Name one owner.** Someone has to own the instructions field, notice when output quality drifts, and re-verify the platform's coverage terms periodically — they change. An assistant with no owner slowly stops matching your program's standards and nobody can say when it started.

---

## Equivalents in other tools

| Tool | Closest feature | Note |
|---|---|---|
| **Claude** | A shared **Project** in the Enterprise workspace | See *Standard / 2 - Set Up in Claude (Projects)*. Check the project's sharing settings — shared projects expose their conversations. |
| **Gemini** | A shared **Gem** | See *Standard / 4 - Set Up in Gemini (Gems)*. Shared Gems live in Google Drive and inherit Drive sharing, including external sharing if your domain allows it. Google has never confirmed whether Gems specifically fall under its agreement — confirm with your administrator. |
| **Google Cloud** | An agent on Gemini Enterprise Agent Platform | A different product under a different agreement than Workspace. Don't assume your Workspace coverage carries over. |
