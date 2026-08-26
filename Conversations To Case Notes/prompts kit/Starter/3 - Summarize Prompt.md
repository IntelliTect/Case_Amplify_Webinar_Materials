# Summarize Prompt

**What this does.** Turns a long conversation into a short, structured summary for the case file.

**How to use it.** Paste the Master Instructions, then the conversation, then this prompt.

**What to check.** Read the Review & Sign-off block *first*, then read the summary against it. Confirm every fact is one the client actually stated, that no identifier you didn't need slipped in, and that nothing is editorialized. Fix, then sign.

**Minimum necessary.** A summary needs the *story*, not the identifiers. You do not need to paste a Social Security number to get a good summary, and this prompt is built to leave it out.

---

## Copy this

```
Summarize this client conversation for the case file. Use these sections:

- Contact & Context (who, when, setting, purpose of the visit)
- Presenting Needs (what the client came in for / what has changed)
- Key Facts (benefits, income, household, housing, health, education — as stated)
- Actions Taken & Next Steps

Keep it brief and factual. Report only what was said in the conversation.
```

---

## Example output

*Using the fictional sample conversation. All names, dates, and numbers are invented.*

> **Contact & Context.** In-person office visit (August 5, 2026) for a SNAP recertification check-in. Client: Marisol Reyes (Client ID CL-2026-04417). Caseworker: Jordan Ellis.
>
> **Presenting Needs.** Client reports a recent job loss and requests help maintaining benefits, arranging childcare so she can return to work, and addressing rent she is at risk of missing.
>
> **Key Facts (as stated).**
>
> - Employment: laid off from warehouse work (last day July 18); previously ~$18.50/hr, ~32 hrs/week; ~2 years there.
> - Benefits: currently receiving $535/month SNAP; recertification paperwork due August 22.
> - Household: client and two dependents, ages 9 and 4; younger child needs childcare.
> - Housing: rent $1,150/month; client reports a late notice from the landlord.
> - Health: client reports a repetitive-strain wrist injury she attributes to warehouse work, which she says limits physical work.
> - Education/goals: high-school diploma plus ~1 year of community college; interested in medical-billing or administrative work.
>
> **Actions Taken & Next Steps.** Referred to a workforce-development program with orientation scheduled August 14, 10:00 AM. Childcare-subsidy application to be started (target submission August 20). One-time rental-assistance form to be emailed to the client today. Client to return SNAP recert paperwork by August 22.
>
> ---
>
> ##### Review & sign-off
>
> **Stated vs. inferred:** The session is dated August 5, 2026 (stated at the top), so all dates resolve to 2026. The children's surname and the client's state are never stated. SSN, phone, email, and street address were intentionally omitted (not needed for a summary).
>
> **Open questions / missing info:** Confirm the recert income-change documents required; confirm childcare-subsidy submission date.
>
> **Reviewed by:** ──────────────────────   **Date:** ──────────────
>
> *AI-drafted. Not part of the record until reviewed and signed by a caseworker.*

---

## What to notice in that example

**The health detail is attributed, not asserted.** "Client reports a repetitive-strain wrist injury she attributes to warehouse work" — not "client has a repetitive strain injury." You are recording a report, not making a finding.

**Nothing decides eligibility.** The summary says the benefit may adjust at recertification; it does not say by how much, or that the client qualifies for anything.

**The identifiers are gone, on purpose.** The sample conversation contains a Social Security number, a phone number, an email address, and a street address. None appear here, and the Review block says so explicitly. That's minimum-necessary working as intended.

**Two facts are marked absent rather than filled in.** The children's surname and the client's state are never spoken in the conversation. A careful AI either writes "not stated" or offers a clearly-flagged guess — both are acceptable. Silently inventing them is not.

---

> **Before this goes anywhere:** a person reads it, corrects it, and signs it. The AI drafted; you decide.
