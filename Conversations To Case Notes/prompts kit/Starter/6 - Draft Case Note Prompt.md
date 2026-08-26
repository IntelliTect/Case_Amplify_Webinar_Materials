# Draft Case Note Prompt

**What this does.** Drafts a case note in whichever format you choose from *8 - Case Note Format Templates*.

**How to use it.** Paste the Master Instructions, then the conversation, then this prompt with your format filled in. If you don't pick one, you get the General-purpose format.

**What to check.** That every line traces back to something in the conversation. That what the client *reported* is clearly distinguished from what was *observed* or *planned*. That there's no diagnosis and no eligibility ruling. And that you agree with every word — because once you sign it, it's your note, not the AI's.

---

## Copy this

```
Draft a case note from this client conversation.

FORMAT: <choose one — General-purpose | SOAP | DAP | GIRP | Case Amplify>
(If no format is given, use General-purpose.)

Follow the chosen format's sections exactly.
- Base every statement on the conversation.
- Attribute clearly: what the client REPORTED vs. what was OBSERVED or PLANNED.
- Objective and non-clinical. Do not diagnose or rule on eligibility.
- Practice minimum-necessary: include the SSN or full identifiers only if the
  note format explicitly requires them (most don't).
```

---

## Which format should I pick?

**General-purpose** is the safe default for benefits, employment, and general social-services case management. If nobody has told you otherwise, use it.

**SOAP, DAP, and GIRP** come from clinical and behavioural-health settings. Use one only if your program or funder expects it — and read the caution about "Assessment" sections in *8 - Case Note Format Templates* before you do.

**Case Amplify** mirrors the structure used in that system.

---

## Example output — General-purpose format

*Using the fictional sample conversation. All names, dates, and numbers are invented.*

> **Contact & Context.** In-person office visit, August 5, 2026. SNAP recertification check-in with Marisol Reyes (Client ID CL-2026-04417). Present: client and caseworker Jordan Ellis.
>
> **Presenting Needs.** Client reports being laid off from warehouse work (last day July 18) and requests support maintaining benefits, arranging childcare to enable a return to work, and addressing at-risk rent. Client reports a repetitive-strain wrist injury she attributes to prior work and states a preference for non-physical roles (medical billing / administrative).
>
> **Actions Taken.** Verified identity and household (client plus two dependents, ages 9 and 4). Reviewed the income change and its likely effect on the SNAP benefit at recertification. Referred client to a workforce-development program and scheduled an orientation (Aug 14, 10:00 AM). Initiated a childcare-subsidy application. Identified potential eligibility for one-time rental assistance given the job loss.
>
> **Plan & Next Steps.**
>
> 1. Caseworker to email the rental-assistance form to the client today.
> 2. Client to return SNAP recert paperwork by Aug 22; caseworker to process the income change.
> 3. Caseworker and client to submit the childcare-subsidy application by Aug 20.
> 4. Client to attend workforce orientation Aug 14, 10:00 AM.
>
> ---
>
> ##### Review & sign-off
>
> **Stated vs. inferred:** Dates resolve to 2026 (session dated Aug 5, 2026). Wrist injury and its effect are the client's report, not a clinical finding. "Likely effect on benefit" reflects the caseworker's stated expectation, not a determination.
>
> **Open questions / missing info:** Confirm the income-change documentation needed for recertification. Confirm childcare-subsidy submission channel and firm deadline.
>
> **Reviewed by:** ──────────────────────   **Date:** ──────────────
>
> *AI-drafted. Not part of the record until reviewed and signed by a caseworker.*

*The same conversation drafted into all five formats is in* **8 - Case Note Format Templates** *— swap the FORMAT line and re-run to watch the note change shape.*

---

## Reading a draft note critically

This is the output where careless review does the most damage, because a case note is a legal record about a real person. Three specific things to look for:

**Attribution creep.** Watch for the AI quietly upgrading a report into a fact. "Client reports a wrist injury she attributes to warehouse work" is a record of what she said. "Client has a repetitive strain injury from warehouse work" is a medical claim you are not making. The first is right. The second is a problem, and it's a one-word edit away.

**Eligibility language.** "Identified potential eligibility for rental assistance" records that you flagged a possibility. "Client is eligible for rental assistance" is a determination. Only the person and process with authority to determine eligibility gets to write the second one.

**Things you did that aren't in the note, and things in the note you didn't do.** The AI only knows what was said out loud. If you did something the conversation didn't mention, add it. If the note credits you with something you only discussed, cut it.

**A note on tone.** These drafts will read as flatter and less warm than notes you write yourself. That's deliberate — a case note is a record, not a narrative, and neutral language protects the client if the file is ever read by someone with less context than you. If it reads a little dry, it's probably working.

---

> **Before this goes anywhere:** a person reads it, corrects it, and signs it. A case note is your professional judgment on the record. The AI can save you the typing; it cannot supply the judgment.
