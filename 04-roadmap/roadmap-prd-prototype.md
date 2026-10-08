# Roadmap, PRD & Prototype (Module 4)

## Your strategic anchors
- **Persona (M2), who are you solving for?:** Lena, the Decide-First Juggler

Role: A salaried, phone-first online shopper who spreads BNPL across Klarna, PayPal and Riverty, using whichever appears at checkout, and who often orders items she may send back.

Goal: To receive and inspect what she bought before any money leaves her account, while keeping a clear picture of what she owes and when, so she never misses a payment or pays reminder fees.

Friction (Moment of Misery): She is forced to abandon "decide first, pay later" whenever Riverty isn't offered, either switching to Klarna or PayPal or paying upfront by debit card and waiting for a refund. Meanwhile her open payments sit across several apps with different due dates and return rules, so she risks losing track and forgetting to pay.
- **Primary success metric (M3), your leading indicator:** Primary success metric

Off-network card transactions per active cardholder per month: the number of card purchases a heavy user makes at merchants that don't offer Riverty at checkout.

How to measure it:

Numerator: card transactions at merchants outside the Riverty checkout network, from issuer-processor data.
Denominator: active cardholders in the month, meaning at least one card transaction.
Segment: heavy users first (the deck's sweet spot is about 82k heavy app users), so it isn't diluted by light users.
- **Moment of misery (M2), the specific friction blocking the goal:** Friction (Moment of Misery): She is forced to abandon "decide first, pay later" whenever Riverty isn't offered, either switching to Klarna or PayPal or paying upfront by debit card and waiting for a refund. Meanwhile her open payments sit across several apps with different due dates and return rules, so she risks losing track and forgetting to pay.
- **Guardrail metric (M3), what must not drop or break:** Guardrails to read alongside it
Merchant impact: partner-merchant checkout conversion should not fall. If card use at partners cannibalises Riverty checkout, the merchant-first constraint is breached.
Payment health: late payments and reminders sent, to check that more use isn't coming with more missed dues.
Trust signals: support contacts about SCHUFA, fees or declines.

## Scan the backlog & set a human baseline
- **My instinctive “quick wins” before touching the AI (2 to 3 feature IDs + why):** Card in Apple Pay and Google Pay - I belive using cards from your wallet makes the most sense and is the most convenient specially for heavy shoppers. I doubt anyone is using physical cards unless they have to. 

Pay-after-you-keep invoice - I think this would be distinct advantage of our card from other credit cards and deliver on the core value of BNPL.

## Audit, override & decide
- **Where did you override the AI? (feature + old vs. new score + why):** Some of the features related to returns and limit displays were rated as high effort but we already basically have the capabilties so i informed AI to overwrite those based on the new information that it lacked before.
- **Did the AI over-value a Sales/Eng request your M2 interviews don’t support?:** N/A
- **Did it underweight something your M3 cohort/funnel data strongly supports?:** No

## Generate your interactive roadmap
- **My “Now” lane (this sprint), the 2 to 3 quick wins I’ll build first:** NOW:
- NR1 · Frictionless onboarding
  What it does: Links her bank with Face ID or Touch ID and gives a fast approval decision.
  Value 4 · Effort 3 · Quick Win
  Rationale: No cardholders means no metric, and users said they'd abandon setup without biometric login (UXR-28, deck MVP).

- NR2 · Card in Apple Pay and Google Pay
  What it does: Adds the virtual Mastercard to her phone wallet so she can pay at merchants outside the Riverty network.
  Value 5 · Effort 3 · Quick Win
  Rationale: It is the precondition for every off-network purchase, though Apple's approval lead time is unknown.

- NR3 · Pay-after-you-keep invoice
  What it does: Creates a per-purchase invoice with a due date, so money leaves her account only after she has decided to keep the item.
  Value 5 · Effort 4 · Major Project
  Rationale: It is the core promise and the heaviest must-have, since production invoicing and settlement still need building.

- NR4 · Return pause
  What it does: Freezes the due date as soon as she reports a return, using the existing two-way return notifications.
  Value 4 · Effort 3 · Quick Win
  Rationale: It protects her at the moment BNPL is for (UXR-17) but needs Risk and Finance rules on pause length and abuse.

- NR7 · One view of what's due
  What it does: Lists every card purchase and open invoice with due dates, updated by instant purchase alerts.
  Value 4 · Effort 2 · Quick Win
  Rationale: It directly answers "losing track" (UXR-09, 12, 23), but only for Riverty purchases, not her Klarna or PayPal balances.

- NR8 · Always-visible remaining limit
  What it does: Shows her total and remaining limit so she knows a purchase will go through.
  Value 4 · Effort 2 · Quick Win
  Rationale: It prevents the declines that would end off-network use, assuming the B2B limit capability carries over.
- **What I cut, and the “no” I’m protecting the scope from:** CUT:
- NR11 · Autopay for small amounts
  What it does: Pays purchases under a threshold she sets (most said 50 or 100 euros) directly from her bank account.
  Value 3 · Effort 3 · Fill-In
  Rationale: Rated 2.3 to 2.4 in 2023 and it needs a direct-debit mandate flow, while the keep-or-return nudge covers the on-time-payments guardrail more cheaply.

- NR12 · Full lost-phone safeguards
  What it does: Offers single-use card numbers for online purchases and blocking the card from another device.
  Value 2 · Effort 3 · Fill-In
  Rationale: The worry is real (UXR-27) but doesn't move off-network use in a pilot, and the standard block-card control ships regardless.

- NR13 · Cashback at partner merchants
  What it does: Pays her money back when she shops with selected merchants, which she can use against an invoice or take to her bank account.
  Value and effort: not scored in this framework
  Rationale: The top-rated feature in 2023 (1.5), but it needs merchant funding and a partner network that doesn't exist, and interchange of about 0.1% can't pay for it, so it is a separate hypothesis.

- NR14 · Physical card
  What it does: Adds a plastic card as a backup for empty or lost phones and for travel.
  Value and effort: not scored in this framework
  Rationale: Rated 2.5 in 2023, two thirds weren't willing to pay the 2.50 euro monthly fee, and 6 of 15 didn't need one.

- NR15 · Consumer credit
  What it does: Offers a loan or revolving credit through the card.
  Value and effort: not scored in this framework
  Rationale: Devalidated in 2023, as 9 of 10 would not use it because they don't want debt, and it needs its own regulatory approval.

- NR16 · Currency converter and rate lock
  What it does: Shows the euro amount before paying abroad and lets her lock an exchange rate for a fee.
  Value and effort: not scored in this framework
  Rationale: Rated 2.2 and partially devalidated, a nice-to-have used mainly on holiday and unrelated to her friction.

- NR17 · Peer-to-peer payments
  What it does: Sends money to a friend's Riverty card by phone number from a pre-funded balance.
  Value and effort: not scored in this framework
  Rationale: Validated at 1.9 but it needs both people on the card, users wanted it funded from their bank account, and it doesn't touch her friction.
- NR10 · "What would you have used?" prompt
  What it does: Asks after each off-network purchase what she would have used otherwise (Klarna, PayPal, debit card, nothing).
  Value 3 · Effort 1 · Fill-In
  Rationale: It is the only way to read the hypothesis, since nothing else shows that off-network use displaces competitors.
- **Prototype/roadmap screenshot link (paste into your deliverables):** https://github.com/koostk-ui/Riverty-Product-School-Koost/blob/main/04-roadmap/riverty_card_roadmap.html
