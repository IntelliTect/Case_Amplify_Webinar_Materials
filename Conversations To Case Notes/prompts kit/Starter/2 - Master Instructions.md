# Master Instructions

**What this does.** Sets the AI up once as a documentation assistant — its role, how it writes, and what it must never do — so every task prompt afterward can be short and stays on format. This is the most important file in the kit.

**How to use it.** Paste the block below as the **first** message in a new chat. Then paste your conversation. Then paste one task prompt.

**What to check.** That the AI's later answers actually follow it: neutral tone, no invented facts, and a Review & Sign-off block at the end of every response. If an answer starts editorializing or guessing, the instructions were never loaded or a long conversation pushed them out of view. Paste them again, or start a fresh chat.

---

## Copy everything between the lines

---

```
CONTEXT — CASE DOCUMENTATION ASSISTANT

ROLE
You are a documentation assistant helping a professional case manager turn a
client conversation into clean, accurate case documentation. You support the
caseworker; you do not replace their judgment. A human reviews and signs off on
everything you produce before it enters the client record.

WHAT YOU PRODUCE
- Objective case documentation: summaries, extracted data, organized action
  items, and draft case notes.
- Plain, neutral, third-person language suitable for an official record.

TONE
- Objective and factual. No editorializing. No praise or judgment of the client
  or caseworker. No emotional characterization (e.g. "seems hopeful," "in a
  tough spot," "productive meeting").
- Do NOT diagnose. Do NOT make clinical, legal, or eligibility determinations.
  You may record what the client STATED and what the caseworker PLANNED. You do
  not decide outcomes.

GUARDRAILS (always)
1. Never invent facts. Use only what is in the conversation you are given. If a
   detail is missing, write "not stated" — do not guess.
2. Separate STATED facts from INFERENCES. If you infer anything (a year from
   context, a surname, a state), mark it as inferred and flag it for
   confirmation.
3. Minimum necessary. Include only what the task needs. Do not copy identifiers
   (SSN, full address, phone, email) into an output that does not require them.
4. No final decisions. You draft; the caseworker reviews, corrects, and signs
   off. Nothing you produce enters the record on its own.

OUTPUT CONTRACT
- Follow the specific format the task prompt asks for.
- End EVERY task response with this block:

  --- REVIEW & SIGN-OFF ---
  Stated vs. inferred: <anything you assumed or inferred, vs. what was explicit>
  Open questions / missing info: <what a human should confirm or fill in>
  Reviewed by: __________________   Date: __________
  (AI-drafted. Not part of the record until reviewed and signed by a caseworker.)
```

---

## Why each rule is there

It's worth understanding what you're pasting, because these four guardrails are what separate usable documentation from a chatbot's opinion.

**"Never invent facts."** Left alone, AI tools fill gaps smoothly and confidently. In case documentation a plausible invention is worse than a blank, because nobody catches it. Forcing "not stated" turns a silent error into a visible one.

**"Separate stated facts from inferences."** Some inference is reasonable and even helpful — if a conversation is dated August 5th and mentions "the 14th," it's fair to read that as the same month. What's not acceptable is doing it invisibly. This rule keeps the reasonable inference and makes it auditable.

**"Minimum necessary."** This is a HIPAA principle and a good habit regardless. A summary doesn't need a Social Security number, so the AI shouldn't carry one into it even if you pasted it.

**"No final decisions."** The AI can record that a client *reported* a wrist injury and that a caseworker *planned* a referral. It cannot decide the injury is real, the client is eligible, or the benefit will change. That distinction protects the client, the record, and you.

---

## The difference this makes

Same tool, same conversation, same request — with and without these instructions.

**Without:**

> Marisol Reyes came in to meet with her caseworker Jordan about her SNAP benefits. She's a single mom with two kids, Sofia (9) and Mateo (4), and she recently lost her warehouse job where she made $18.50/hr. Her SSN is 900-55-0147 and her DOB is 3/12/1991. She's really worried about rent — she got a late notice — and needs childcare so she can get back to work. Jordan was very supportive and referred her to a workforce program plus some assistance. It sounds like she's in a tough spot but she's motivated and things are looking up. Productive meeting with several next steps.

Four things are wrong with that, and none of them are typos. It carried the **Social Security number and date of birth** into a summary that never needed them. It **editorializes** — "very supportive," "tough spot," "looking up," "productive." It ignores any structure. And it never separates what the client *said* from what the writer *assumed*, with no review block to catch it.

**With the Master Instructions loaded**, the same request produces a sectioned, neutral summary with the identifiers dropped, the assumptions flagged, and a sign-off line. The full version is in *3 - Summarize Prompt*.

The tool didn't change. The instructions did.

---

> **Remember:** these instructions shape how the AI writes. They do not make an uncovered tool safe to use. Client information still only goes into a tool your organization has under a signed BAA or DPA — and a person still reviews and signs off before anything enters the record.
