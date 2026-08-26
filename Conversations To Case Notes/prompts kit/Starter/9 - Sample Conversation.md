# Sample Conversation

**A fictional client conversation to practise on.** Every prompt in this folder shows its worked example against this transcript, so you can run any of them yourself, compare what you get to what's shown, and build some confidence before you touch a real client file.

> ### ⚠️ Everything below is invented
> No real person, case, or record is involved. The phone number uses the reserved `555` prefix, the Social Security number uses a `900` prefix that has never been issued, the email address uses the reserved `.test` domain, and the client, city, and ID numbers are fabricated.
>
> **Practise on this, not on a real conversation** — including while you're checking whether your organization's tool is covered.

**Scenario.** A SNAP recertification and workforce-development referral check-in. In-person office visit, recorded with the client's consent.
**Participants.** Jordan Ellis (caseworker) and Marisol Reyes (client).

---

## The conversation

**Jordan (Caseworker):** Thanks for coming in, Marisol. For the record, today is August 5th, 2026. Before we get into it, let me confirm a few details so I'm in the right record — can you give me your full name and date of birth?

**Marisol:** Sure — Marisol Reyes, and my date of birth is March 12th, 1991.

**Jordan:** Great. And to verify your identity on the benefits side, can you confirm your Social Security number?

**Marisol:** It's 900‑55‑0147.

**Jordan:** Perfect, that matches. I've got your client ID as CL‑2026‑04417. Is the best number for you still the one ending in 0134?

**Marisol:** Yes, (555) 213‑0134. And my email is the same, m.reyes@example‑mail.test.

**Jordan:** And you're still at 482 Larkfield Avenue, Apartment 3B, here in Millbrook?

**Marisol:** Yes, same place. 97000.

**Jordan:** Okay. So the main reason we're meeting is your SNAP recertification — that paperwork is due August 22nd, and I want to make sure we don't let it lapse. But you also mentioned on the phone that some things have changed. Walk me through it.

**Marisol:** Right. So I was working at the distribution warehouse — I was there almost two years. They downsized and my last day was July 18th. I was making $18.50 an hour, around 32 hours a week. Now it's nothing.

**Jordan:** I'm sorry, that's a hard hit. That change in income actually helps your recertification — your benefit is likely to adjust. Right now you're receiving $535 a month in SNAP, is that right?

**Marisol:** Yes, $535.

**Jordan:** Okay. Let's make sure the household is current. It's you and your two kids?

**Marisol:** Yes. My daughter Sofia is nine — she's at Larkfield Elementary. And my son Mateo just turned four. That's actually part of the problem — if I go back to work, I need childcare for Mateo, and I can't afford it out of pocket right now.

**Jordan:** That's exactly what the childcare subsidy is for, and I can help you start that application. Are you looking to go back into warehouse work, or something different?

**Marisol:** Honestly, something different. I hurt my wrist at the warehouse — it's a repetitive strain thing, the doctor said, from the lifting and scanning all day. It flares up. So I don't think I can go back to that kind of physical work. I was thinking maybe something like medical billing, or office and admin work. I finished high school and I did about a year of community college.

**Jordan:** That's a really reasonable direction, and it lines up well with a program I want to refer you to. It's a workforce-development program — they do job-readiness, résumé help, and they have training tracks including administrative and medical-office work. I can get you into an orientation. There's one on August 14th at 10 in the morning — does that work?

**Marisol:** The 14th at 10 works. I'll be there.

**Jordan:** I'll put you down. Now — the other thing you mentioned was rent.

**Marisol:** Yeah. My rent is $1,150 a month, and with no income coming in I'm worried. I actually already got a late notice from my landlord. I don't know what I'm going to do about this month.

**Jordan:** Okay. There's a one-time rental-assistance program you may qualify for, especially given the job loss. I'll email you the application form today so you can get it started right away — the sooner that's in, the better.

**Marisol:** That would really help. Thank you.

**Jordan:** Let me read back the plan so we're on the same page. One: I'll email you the rental-assistance form today. Two: your SNAP recertification paperwork is due August 22nd — get that back to me before then and we'll process the income change. Three: I'll start your childcare-subsidy application, and we need to submit that by August 20th. Four: workforce orientation, August 14th at 10 a.m. Does that all sound right?

**Marisol:** Yes, that's everything.

**Jordan:** Good. I know this is a lot at once, but you're doing the right things. Let's get you back on your feet.

**Marisol:** Thank you, Jordan. I really appreciate it.

---

## Answer key — check your own work

Use this to score what the AI gave you. It is not a grading sheet so much as a way to see *where* AI output needs a human, and the two rows marked "not stated" are the most instructive part.

### Identifiers

| Field | Correct value | Note |
|---|---|---|
| Client name | Marisol Reyes | |
| Date of birth | 03/12/1991 | A date is itself an identifier |
| **SSN** | **900‑55‑0147** | The one field that makes extraction a covered-tool-only task |
| Client ID | CL‑2026‑04417 | |
| Phone | (555) 213‑0134 | |
| Email | m.reyes@example‑mail.test | |
| Address | 482 Larkfield Ave, Apt 3B, Millbrook, 97000 | **State is never stated** — the ZIP implies Oregon, but confirm rather than assume |
| Dependent 1 | Sofia, age 9, Larkfield Elementary | A minor plus a named school is sensitive. **Surname never stated** |
| Dependent 2 | Mateo, age 4 | **Surname never stated** |

### Case data

| Field | Correct value |
|---|---|
| Session date | 08/05/2026 — stated out loud at the start |
| Prior employer | Distribution warehouse, about 2 years |
| Prior wage / hours | $18.50/hr, ~32 hrs/wk |
| Employment end date | 07/18/2026 |
| Current SNAP benefit | $535/mo |
| SNAP recertification deadline | 08/22/2026 |
| Rent | $1,150/mo, late notice received |
| Health note | Repetitive-strain wrist injury, client-reported |
| Education | High-school diploma plus ~1 year community college |
| Employment interest | Medical billing / office / administrative |

### Action items and referrals

| Item | Owner | Due |
|---|---|---|
| Email rental-assistance form | Caseworker | Today |
| Submit childcare-subsidy application | Caseworker + client | by 08/20/2026 |
| Return SNAP recertification paperwork | Client | by 08/22/2026 |
| Workforce orientation | Client | 08/14/2026, 10:00 AM |
| Referral: workforce-development program | — | — |
| Referral: childcare subsidy | — | — |
| Referral: one-time rental assistance | — | — |

---

## The two rows worth studying

**The year is stated, so dates are certain.** Jordan says the date out loud at the top — "today is August 5th, 2026" — so every later "August 14th" and "the 22nd" resolves to 2026 without guessing. That is not luck; it's a habit worth copying. Say the date at the start of a recorded conversation and you remove a whole category of AI error.

**Two values are never spoken, and that's the point.** The children's **surname** and the client's **state** appear nowhere in the conversation. A careful AI will either write "not stated" or offer a clearly-flagged guess ("Reyes", "OR") for you to confirm. **Both of those are correct answers.** What is not acceptable is quietly filling them in — a child's legal surname in an official record is not something to infer silently.

So when you score your own run, don't count a blank as a miss. Count an *unflagged guess* as the miss. That distinction is the whole reason the Review & Sign-off block exists.
