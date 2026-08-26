# Organize Action Items Prompt

**What this does.** Reshapes a conversation into something you can act on — a task list with owners and due dates, the referrals being made, and every deadline in order.

**How to use it.** Paste the Master Instructions, then the conversation, then this prompt.

**What to check.** That every owner and date came from the conversation rather than being assumed, that nothing agreed to was dropped, and that the timeline order is actually right.

---

## Copy this

```
Turn this client conversation into an actionable view for the caseworker.
Produce three parts:

1. ACTION ITEMS — a table: Item | Owner | Due date. Include appointments.
2. REFERRALS — programs the client is being connected to.
3. DEADLINE TIMELINE — every dated item in chronological order, soonest first.

Use only the owners and dates stated in the conversation. Mark anything you
inferred (e.g. an assumed year). Do not add tasks that were not discussed.
```

---

## Example output

*Using the fictional sample conversation. All names, dates, and numbers are invented.*

**1. Action Items**

| Item | Owner | Due date |
|---|---|---|
| Email rental-assistance form to client | Caseworker | Today (Aug 5, 2026) |
| Submit childcare-subsidy application | Caseworker + client | By Aug 20 |
| Return SNAP recertification paperwork | Client | By Aug 22 |
| Attend workforce-development orientation | Client | Aug 14, 10:00 AM |

**2. Referrals**

- Workforce-development program (job-readiness, résumé help, admin / medical-office training tracks)
- Childcare-subsidy program
- One-time rental-assistance program

**3. Deadline Timeline (soonest first)**

1. **Aug 5, 2026 (today)** — caseworker emails rental-assistance form.
2. **Aug 14, 10:00 AM** — workforce orientation.
3. **Aug 20** — childcare-subsidy application submitted.
4. **Aug 22** — SNAP recert paperwork returned.

> ---
>
> ##### Review & sign-off
>
> **Stated vs. inferred:** All dates resolve to 2026 (session dated Aug 5, 2026); "Today" = Aug 5, 2026. No owners were assumed — each was stated by the caseworker in the read-back at the end of the conversation.
>
> **Open questions / missing info:** Does the childcare-subsidy application have a hard portal deadline, or is Aug 20 an internal target? Confirm who submits the recertification versus who processes it.
>
> **Reviewed by:** ──────────────────────   **Date:** ──────────────
>
> *AI-drafted. Not part of the record until reviewed and signed by a caseworker.*

---

## What to notice in that example

**"Owner" is only as good as the conversation.** This example works cleanly because the caseworker read the plan back at the end and named who was doing what. If your conversation doesn't do that, the AI has to guess at ownership — and it will. Read that column carefully, or get in the habit of reading the plan back before the conversation ends. It makes the documentation better and it's good practice with the client anyway.

**"Today" is a trap worth knowing about.** The AI will faithfully copy "today" from the conversation. If you run this prompt a week later, "today" now means something different to whoever reads the note. Resolve relative dates to actual dates before this goes in the record.

**The open question about Aug 20 is the useful kind.** A hard portal deadline and an internal target look identical in a transcript but behave very differently when one is missed. Flagging the difference is exactly the sort of thing a review block should surface.

---

> **Before this goes anywhere:** a person reads it, corrects it, and signs it.
