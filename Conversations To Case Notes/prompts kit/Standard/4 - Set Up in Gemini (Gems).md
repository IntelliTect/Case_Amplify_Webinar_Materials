# Set Up in Gemini — Gems

**Time:** about ten minutes, once. **You need:** a paid Google Workspace account where an administrator has accepted the agreement, and a computer (not a phone).

---

## Before you start

A **Gem** is Google's saved-instructions feature — in Google's words, *"a customized version of Gemini that helps you tackle repetitive tasks."* Build it once and it's available in the Gemini app **and** in the Gemini side panel of Gmail, Docs, Drive, and Sheets.

Confirm all three of these before you begin:

- You're in your organization's **Google Workspace** account — not a personal Google account, and **not** Google AI Pro or Ultra. The consumer Gemini app cannot be covered at all; a personal account has no administrator, so there's no way to put an agreement in place.
- Your administrator has **accepted the agreement**, and Gemini is turned on as a **Core Service** rather than an Additional Product. Google is explicit that access as an Additional Product is not covered — and it's the same app either way, so you can't tell by looking.
- Your edition includes Gemini as a core service. **Business Base, Essentials Starter, legacy free G Suite, and custom editions don't**, so they can't be covered for Gemini even with an agreement signed.

If you're unsure about any of those, ask your administrator. It's a two-minute question for them.

---

## The steps

Gems can only be **created or edited on the web.** The mobile app can use them but not build them.

1. On a computer, go to **gemini.google.com**, signed in to the covered Workspace account.
2. Click **Open Sidebar → Gems → New Gem**.
3. Name it **Case Documentation Assistant**.
4. Paste the **entire** Master Instructions block from *Starter / 2 - Master Instructions* into the **instructions** field.
5. *Optional:* under **Knowledge**, click **Add files** and attach *Starter / 8 - Case Note Format Templates*. Read the caution below first.
6. Click **Save**.

---

## Using it day to day

1. Open the Gem — from **gemini.google.com**, or by clicking **Ask Gemini** in the side panel of Gmail, Docs, Drive, or Sheets.
2. Paste the client conversation.
3. Paste one task prompt from the Starter folder.
4. Read the Review & Sign-off block, correct, and sign.

---

## ⚠️ Three Gemini-specific cautions

These are real, and none of them are obvious from the interface.

**1. Never use Gemini in Chrome or Gemini Notebook for client information.** Google explicitly excludes both from its agreement — even when the rest of your Workspace subscription is covered. Google recommends administrators turn Gemini in Chrome off entirely. **Gemini Notebook** (formerly NotebookLM) is the more dangerous of the two, because it's a core service in most editions, it holds uploaded source documents, and it is exactly where someone would think to put a transcript. Core-service status is not coverage.

**2. Google has never said whether Gems specifically are covered.** The Gemini app *is* on Google's covered-functionality list as of May 2026, and a Gem is a feature inside that app — so the reasoning is sound. But Google names Gems nowhere in its compliance documentation, neither included nor excluded, and its own FAQ warns that *"some features might be blocked for customers who have signed the HIPAA Business Associate Amendment"* without saying which features. **Ask your administrator to confirm before you put client information into a Gem.** Don't infer it, and don't let this document be your authority on it.

**3. Shared Gems live in Google Drive and inherit Drive's sharing.** Google states that *"shared Gems are stored and shared in Google Drive, so the sharing settings for Drive also apply."* If your domain allows external Drive sharing, a shared Gem can be shared outside your organization. Where an *unshared* Gem's uploaded knowledge files physically live — and whether they inherit your Drive or Vault retention — is **not documented by Google at all**.

Which leads to a simple working rule: **attach templates to a Gem, never client files.**

---

## Two other things worth knowing

**Your Gemini activity history is on by default,** and only an administrator can turn it off. They also set how long it's kept — 3, 18, or 36 months. If your organization has record-retention obligations, that setting is the lever, and it's worth knowing what yours is.

**Gems may not be Gems for long.** An unconfirmed report from August 2026 suggests Google may migrate Gems to a feature called **Skills** later in the year. Skills today requires a personal account with a consumer subscription and does **not** support work or school accounts — so it isn't an option for this audience as things stand. Re-check before you build training around this file.

---

## Test it

Open the Gem. Paste a few sentences of any conversation. Ask for a case-file summary.

**Working:** sections, neutral tone, a Review & Sign-off block, with no instructions pasted.
**Not working:** check that the instructions actually saved, and that you're in the Gem rather than a plain Gemini chat.
