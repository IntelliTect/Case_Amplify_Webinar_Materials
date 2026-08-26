# De-Identify Prompt

**What this does.** Replaces identifying details with labeled placeholders — `[CLIENT NAME]`, `[SSN]`, `[DATE]`, `[ADDRESS]` and so on — so the narrative can be worked on with less exposure.

**How to use it.** Paste the text you want to clean, then this prompt. You do **not** need the Master Instructions first. Then read the "what I replaced" list it produces and check nothing slipped through.

**What to check.** Read the redacted text back and hunt for stragglers — a name mid-sentence, a stray date, a ZIP code. Automated redaction misses things, reliably. A person has to confirm.

---

## When to use this — and when it can't help

**Use it when:**

- You have to use a tool your organization does **not** have under an agreement, and the task only needs the *story* — summarizing, drafting a narrative. Strip the identifiers first.
- You're already in a covered tool but want an extra layer of care, or the output is going somewhere less controlled.

**It cannot help when the task *is* to capture the identifiers.** Extracting a Social Security number, date of birth, or address into fields (see *4 - Extract Data Prompt*) can't be de-identified first — the identifiers are the deliverable. **That task can only run in a covered tool.** There is no workaround, and looking for one is how mistakes happen.

### Two things people get wrong about this

**De-identified is not the same as not sensitive.** The rules cover *identifiers*. They don't cover dollar amounts, wages, rent, or a description of an injury. Strip every identifier from the sample conversation and you still have a document about a specific person's finances and health. Treat it accordingly.

**It's all-or-nothing, and even then it's not automatic.** Text stops being protected health information only when **all 18 categories** below are removed **and** you have no reason to think what remains could still identify the person. A small town plus an unusual job plus a rare condition can identify someone with every listed identifier gone. A partial redaction is still protected information — keep it in the covered tool.

Which is why, for most real work, the better move is a covered tool where you keep the real dates and simply don't paste what the task doesn't need. Redaction is what you do when you have no covered option — not a shortcut to using a free one.

---

## Copy this

```
De-identify the text below so it contains no HIPAA Safe-Harbor identifiers.
Replace each of the 18 categories with a labeled placeholder in [BRACKETS].
Keep the narrative and non-identifying facts (dollar amounts, program names,
generic job titles) intact.

Replace:
1.  Names (client, family, staff) -> [CLIENT NAME] / [CHILD NAME] / [CASEWORKER]
2.  Geographic detail smaller than a state (street, city, county, ZIP)
        -> [ADDRESS] / [CITY] / [ZIP]
3.  All dates except the year, and any age 90+ -> [DATE] / [AGE 90+]
4.  Phone numbers -> [PHONE]
5.  Fax numbers -> [FAX]
6.  Email addresses -> [EMAIL]
7.  Social Security numbers -> [SSN]
8.  Medical record numbers -> [MRN]
9.  Health-plan / beneficiary numbers -> [PLAN ID]
10. Account numbers -> [ACCOUNT #]
11. Certificate / license numbers -> [LICENSE #]
12. Vehicle IDs / license plates -> [VEHICLE ID]
13. Device IDs / serial numbers -> [DEVICE ID]
14. Web URLs -> [URL]
15. IP addresses -> [IP]
16. Biometric identifiers -> [BIOMETRIC]
17. Full-face photos / comparable images -> [PHOTO]
18. Any other unique identifying number, characteristic, or code (client/case
        ID, a school name tied to a child, etc.) -> [ID] / [SCHOOL NAME]

After the redacted text, list what you replaced, by category, so a human can
verify nothing was missed. Do not remove non-identifying facts.
```

---

## Example output

*An excerpt, using the fictional sample conversation.*

> **[CASEWORKER]:** Thanks for coming in, [CLIENT NAME]. Before we get into it, let me confirm a few details so I'm in the right record. Can you give me your full name and date of birth?
>
> **[CLIENT NAME]:** Sure — [CLIENT NAME], and my date of birth is [DATE].
>
> **[CASEWORKER]:** And to verify your identity on the benefits side, can you confirm your Social Security number?
>
> **[CLIENT NAME]:** It's [SSN].
>
> **[CASEWORKER]:** Perfect, that matches. I've got your client ID as [ID]. Is the best number for you still the one ending in [ID]?
>
> **[CLIENT NAME]:** Yes, [PHONE]. And my email is the same, [EMAIL].
>
> **[CASEWORKER]:** And you're still at [ADDRESS], here in [CITY]?
>
> **[CLIENT NAME]:** Yes, same place. [ZIP].
>
> **[CASEWORKER]:** Okay. So the main reason we're meeting is your SNAP recertification — that paperwork is due [DATE]…
>
> **[CLIENT NAME]:** Right. I was working at the distribution warehouse almost two years. They downsized and my last day was [DATE]. I was making $18.50 an hour, around 32 hours a week. Now it's nothing.
> *(…continues; every date becomes [DATE].)*
>
> **[CLIENT NAME]:** My daughter [CHILD NAME] is nine — she's at [SCHOOL NAME]. And my son [CHILD NAME] just turned four…
>
> **What I replaced:** Names → [CLIENT NAME] (client, throughout), [CASEWORKER], [CHILD NAME] ×2. Dates → date of birth, layoff date, SNAP deadline, orientation date, childcare deadline (all [DATE]). Also: SSN, client ID (and the "ending in" digits), phone, email, street address, city, ZIP, and the child's school. **Left intact (not identifiers):** wage $18.50/hr, ~32 hrs/wk, $535/mo benefit, $1,150 rent, the wrist-injury note, "distribution warehouse," "community college."

---

## The point of that example

Look at what the redaction costs you. **Every actionable date is now `[DATE]`** — the layoff, the recertification deadline, the orientation appointment. The plan is unusable as a plan. You cannot work a caseload from that document.

That is not a flaw in the prompt. It's what the rules require, and it's the clearest argument for keeping this work in a covered tool where you keep the real dates and simply leave out what the task doesn't need.

Two smaller things worth noticing. The school name is redacted even though it isn't obviously an identifier — a specific elementary school attached to a nine-year-old narrows the field considerably. And the dollar amounts survive, because they aren't on the list, which is exactly why "de-identified" doesn't mean "safe to leave anywhere."

---

## Checking the output

Read the redacted text yourself, start to finish. Automated redaction is good at the obvious instances and bad at the ones buried mid-sentence — a first name used casually, a date written as words, a partial phone number like "the one ending in 0134."

If you find even one straggler, treat the whole document as still protected and keep it in your covered tool.

> **A caution about the "trimmed" version.** Some people prefer a lighter pass: strip the identity fields but keep the appointment dates so the note stays usable. That's a reasonable working habit, but it is **not** de-identification. Trimmed text is still protected information and still belongs only in a covered tool. Don't let "trimmed" and "de-identified" become the same word on your team.
