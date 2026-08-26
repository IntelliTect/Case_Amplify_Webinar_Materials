# Extract Data Prompt

**What this does.** Pulls the discrete facts out of a conversation into clean CSV — the format spreadsheets open — so it lines up with your intake fields.

**How to use it.** Paste the Master Instructions, then the conversation, then this prompt. You'll get three labeled blocks. Copy a block into a spreadsheet, or save it as a file ending in `.csv` and open it.

**What to check.** Spot-check the values against the source — especially anything the Review block flags as *inferred*. Confirm no field was invented. A blank or "not stated" is a correct answer; a confident wrong value is the thing to hunt for.

---

## ⚠️ Read this before using this prompt

**This is the one task that needs the identifiers themselves.** It extracts the Social Security number, date of birth, address, and phone number into fields. You cannot strip those out first — they *are* what the task produces.

**So this prompt may only be run in a tool your organization has under a signed BAA or DPA.** There is no compliant way to do this one in a free or uncovered tool, and no amount of careful redaction changes that. If you're not certain your tool is covered, stop and ask.

---

## Copy this

```
Extract the key information from this client conversation into CSV.
Output THREE separate, labeled CSV blocks — nothing else between them but the label line.

BLOCK 1 — "IDENTIFIERS"
Columns: Field,Value,Sensitive
Rows to capture (only if stated): Client name, Date of birth, SSN, Client ID,
Phone, Email, Address, and one row per dependent (name, age, school if given).
Set Sensitive to Yes for every identifier row.

BLOCK 2 — "CASE DATA"
Columns: Field,Value,Sensitive
Capture: the session date, prior employer & tenure, prior wage/hours, employment
end date, current benefit amount(s), benefit deadlines, rent (+ status), health
notes, education, employment interest. Set Sensitive to Yes only for health details.

BLOCK 3 — "ACTION ITEMS & REFERRALS"
Columns: Item,Owner,Due Date,Type
Type is one of: Action item, Appointment, Referral. Leave Owner/Due Date blank
for referrals.

RULES
- Valid CSV: wrap any value that contains a comma in double quotes.
- Use only values stated in the conversation. Write "not stated" if missing;
  never invent a value.
- If you inferred a value (e.g. a year from context, a surname), put the value
  in the cell AND note it in the Review & Sign-off block as inferred.
```

---

## Why three blocks instead of one table

Because the three kinds of information have different shapes. Identifiers and case data are simply field-and-value pairs. Action items need an owner and a due date. Forcing all of that into one table would leave most cells empty and make it harder to read and harder to check.

Three blocks also means each one drops straight into its own worksheet, so comparing what the AI produced against what you expected is a quick side-by-side rather than a hunt.

**If your team would rather import one file**, ask for a single table with the columns `Category, Field, Value, Owner, DueDate, Sensitive` and filter by Category. Same information, one file, slightly harder to read.

---

## Example output

*Using the fictional sample conversation. All names, dates, and numbers are invented.*

**BLOCK 1 — IDENTIFIERS**
```csv
Field,Value,Sensitive
Client name,Marisol Reyes,Yes
Date of birth,03/12/1991,Yes
SSN,900-55-0147,Yes
Client ID,CL-2026-04417,Yes
Phone,(555) 213-0134,Yes
Email,m.reyes@example-mail.test,Yes
Address,"482 Larkfield Ave, Apt 3B, Millbrook, 97000",Yes
Dependent 1,"Sofia, age 9, Larkfield Elementary",Yes
Dependent 2,"Mateo, age 4",Yes
```

**BLOCK 2 — CASE DATA**
```csv
Field,Value,Sensitive
Session date,08/05/2026,No
Prior employer,Distribution warehouse (~2 yrs),No
Prior wage / hours,"$18.50/hr, ~32 hrs/wk",No
Employment end date,07/18/2026,No
Current SNAP benefit,$535/mo,No
SNAP recert deadline,08/22/2026,No
Rent,"$1,150/mo (late notice received)",No
Health note,Repetitive-strain wrist injury (steers away from manual work),Yes
Education,HS diploma + ~1 yr community college,No
Employment interest,Medical billing / office / admin,No
```

**BLOCK 3 — ACTION ITEMS & REFERRALS**
```csv
Item,Owner,Due Date,Type
Email rental-assistance form,Caseworker,Today,Action item
Submit childcare-subsidy application,Caseworker + client,08/20/2026,Action item
Return SNAP recert paperwork,Client,08/22/2026,Action item
Workforce orientation,Client,"08/14/2026, 10:00 AM",Appointment
Referral: workforce-development program,,,Referral
Referral: childcare subsidy,,,Referral
Referral: one-time rental assistance,,,Referral
```

> ---
>
> ##### Review & sign-off
>
> **Stated vs. inferred:** The session is dated August 5, 2026 (stated at the start), so every month and day resolves to 2026 — the year is **stated, not guessed**. Two values are never stated and are shown as "not stated": the dependents' **surname** and the **state**. SSN captured verbatim as spoken.
>
> **Open questions / missing info:** Confirm the dependents' legal surnames and the client's state against the file. Confirm "Today" resolves to the actual visit date for the rental-assistance action.
>
> **Reviewed by:** ──────────────────────   **Date:** ──────────────
>
> *AI-drafted. Not part of the record until reviewed and signed by a caseworker.*

---

## How to check this output in about a minute

**Look at the Review block first.** It tells you where to aim your attention. Everything it flags as inferred is a value you should confirm against the file.

**Then check the two things AI gets wrong most often.**

*Dates.* Anything with a month and day but no year is a guess unless the conversation states the year somewhere. In this example it does — the caseworker says the date out loud at the start — so the years are certain. In a real transcript that may not be true.

*Names that were never spoken.* The sample conversation says "Sofia" and "Mateo" and never gives a surname. Assuming "Reyes" is reasonable, and it may well be right — but it's an assumption about a child's legal name in an official record. Either "not stated" or a clearly-flagged guess is a pass here. A quietly-inserted "Sofia Reyes" is not.

**"Not stated" is a correct answer.** If you find yourself annoyed that the AI left a cell blank, check the transcript before you fill it in. Usually the AI is right and the information genuinely isn't there.

---

> **Before this goes anywhere:** a person reads it, corrects it, and signs it. And remember what this file contains — extracted identifiers belong only in your covered system, not in an email or a shared drive.
