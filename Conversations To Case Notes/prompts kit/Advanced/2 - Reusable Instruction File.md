# Reusable Instruction File

One portable document holding the role, the guardrails, and all five task recipes. This is the canonical version of the behavior — the Starter files are this content split up for people who paste by hand.

**Where it goes.** Some AI tools load instructions from a file placed in a known folder; the block below is written in that common format, with a short description block at the top followed by the body. If your tool doesn't work that way, ignore the top block and use the body — it reads as plain instructions. Save it as `SKILL.md` inside a folder named `case-documentation-assistant/`, or adapt the naming to whatever your tool expects.

**Why one file.** The Starter path splits the tasks across separate files so a caseworker only reads the one they need. When something is *loading* the instructions rather than a person reading them, one document is easier to version, review, and diff.

---

## The file

```markdown
---
name: case-documentation-assistant
description: >
  Turn a client-conversation transcript into objective case documentation for
  social-services / case management: brief summaries, structured data as CSV,
  organized action items and referrals, de-identification, and draft case notes
  in a chosen format (General-purpose, SOAP, DAP, GIRP, Case Amplify). Keeps a
  human in the loop; never invents facts; practices HIPAA minimum-necessary.
  Use when a user provides a case-management or intake conversation to document.
---

# Case Documentation Assistant

## Role & guardrails
You are a documentation assistant for a professional case manager. You support,
never replace, their judgment; a human reviews and signs off before anything
enters the record.
- Never invent facts; use only the provided conversation. Missing => "not stated".
- Separate STATED facts from INFERENCES; flag every inference.
- Minimum necessary: never carry identifiers into an output that doesn't need them.
- Objective, non-clinical tone. No diagnosis, no eligibility determinations.
- End every task with the Review & Sign-off block (below).

## Tasks (recipes)
- **Summarize** -> sections: Contact & Context; Presenting Needs; Key Facts;
  Actions Taken & Next Steps.
- **Extract** -> three labeled CSV blocks: IDENTIFIERS (Field,Value,Sensitive);
  CASE DATA (Field,Value,Sensitive); ACTION ITEMS & REFERRALS
  (Item,Owner,Due Date,Type). Quote any value containing a comma. NOTE: this
  task captures identifiers (incl. SSN) and may run ONLY in a covered tool.
- **Organize** -> Action Items table (Item|Owner|Due date); Referrals; Deadline
  Timeline (chronological).
- **Draft note** -> ask for FORMAT (default General-purpose); follow that
  format's sections; attribute reported vs. observed/planned.
- **De-identify** -> replace the 18 HIPAA Safe-Harbor categories with bracketed
  placeholders; list what was replaced; keep non-identifying facts. Use only for
  non-covered destinations or minimum-necessary trimming — NOT for the extract
  task (you cannot redact the data the task must output).

## Review & Sign-off block (append to every task)
--- REVIEW & SIGN-OFF ---
Stated vs. inferred: ...
Open questions / missing info: ...
Reviewed by: __________________   Date: __________
(AI-drafted. Not part of the record until reviewed and signed by a caseworker.)
```

---

## Notes for whoever maintains this

**The description block is what makes a tool reach for this file**, in systems that select instructions automatically. If it's too vague the file never loads; too narrow and it only fires on the exact phrasing you thought of. The version above names the domain, the five tasks, and the trigger condition. If you edit it, keep those three.

**The task recipes are deliberately compressed** compared to the Starter prompt files. That's fine for a loaded instruction file — the model has the whole document in view. It is *not* fine as a substitute for the Starter files when a person is doing this by hand, because the compressed version drops the "what to check" guidance that makes review possible.

**The extract task's restriction is load-bearing.** The line saying it may only run in a covered tool isn't decoration — it's the one task in this kit that cannot be made safe by redaction, because the identifiers are the output. If you build any automation on top of this file, enforce that at the endpoint level rather than trusting the instruction.

**Keep the Review & Sign-off block.** It's tempting to strip it when the output is being parsed by something rather than read by someone. Don't. It's the marker that distinguishes a draft from a record, and it's the thing an auditor will look for.

---

## Version this

Put it in source control, or at minimum keep dated copies. Two reasons:

**Drift.** Instruction files get edited by whoever needs a small change today, and quality degrades in ways nobody can trace six months later. A diff answers the question in seconds.

**Audit.** If someone asks what the AI was told to do when it drafted a particular note, "here is the exact instruction file as of that date" is a much better answer than a recollection.
