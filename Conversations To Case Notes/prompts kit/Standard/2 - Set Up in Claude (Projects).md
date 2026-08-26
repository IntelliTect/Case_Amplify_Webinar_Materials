# Set Up in Claude — Projects

**Time:** about ten minutes, once. **You need:** access to your organization's Claude Enterprise workspace.

---

## Before you start

Confirm you're in the **Claude Enterprise** workspace your organization has under a signed agreement — or that you're using the Anthropic API.

**Claude Free, Pro, Max, and Team cannot be covered.** Anthropic states it plainly: Team plans and individual plans can't enable HIPAA. If you're on one of those, stop here and talk to whoever manages your software. Don't build this in a personal account.

---

## The steps

1. Sign in to your organization's **Claude Enterprise** workspace.
2. Go to **Projects → Create Project**. Name it **Case Documentation Assistant**.
3. Open the project's **instructions** field (sometimes labeled custom instructions).
4. Paste the **entire** Master Instructions block from *Starter / 2 - Master Instructions* — everything between the lines, from `CONTEXT — CASE DOCUMENTATION ASSISTANT` down to the last line of the sign-off block.
5. **Save.**
6. *Optional but useful:* add *Starter / 8 - Case Note Format Templates* as a project knowledge file. Then "draft a SOAP note" can pull the exact sections instead of relying on the AI's general knowledge of the format.

---

## Using it day to day

1. Open a **new chat inside the project**. This matters — a chat started outside the project doesn't get the instructions.
2. Paste the client conversation.
3. Paste one task prompt from the Starter folder.
4. Read the Review & Sign-off block, correct what's wrong, and sign.

---

## Test it

New chat inside the project. Paste two or three sentences of any conversation. Ask: *"Summarize this conversation for the case file."*

**Working:** neutral tone, the four sections, a Review & Sign-off block at the end — with no instructions pasted.

**Not working:** a friendly paragraph, no sections, no review block. The instructions didn't save, or you're in a chat outside the project.

---

## Keeping it clean

**Keep the project in the covered workspace.** Don't fork or recreate it in a personal account for convenience.

**Watch who else is in it.** If your workspace shares projects across a team, everyone with access to the project can see the conversations in it — which means client conversations. Check the sharing settings before you paste anything real, not after.

**Revisit the instructions when something drifts.** If output quality slips over a few weeks, first check whether someone edited the project instructions. That field is the single point of control, which is its strength and its risk.
