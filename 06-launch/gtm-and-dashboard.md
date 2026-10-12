# GTM Launch Plan, Riverty business-unit case

| Field | Value |
|---|---|
| Feature | pay-after-you-keep invoice, delivered through the card offer to already-onboarded heavy users |
| Goal | Conversion |
| Launch tier | M, Targeted |

## Goal & Audience
- **Goal:** Conversion, Specifically, activation: an eligible heavy user takes up the card and makes a first purchase outside the Riverty network. That is also the first decision gate in your experiment, so the go-to-market plan and the test should chase the same number.

our audience already knows Riverty. The launch group is fully onboarded heavy app users, which Riverty owns and can reach directly. Awareness isn’t what’s missing for them.
The barrier is trust and reason, not visibility. The 2023 research shows SCHUFA fear, doubt about who is behind Riverty, and “one more payment option is one too much.” Those are conversion problems.
The 2023 fake door shows the gap. About 17.5% of exposed app users clicked the card teaser, but only 5% clicked “keep me informed” (a weak signal at that). Interest was there, commitment wasn’t.
Activation is what your test decides. Ship, extend and stop all depend on activation first, then off-network use.
- **Target audience:** Lena, the Decide-First Juggler: A salaried, phone-first online shopper who spreads BNPL across Klarna, PayPal and Riverty, using whichever appears at checkout, and who often orders items she may send back.

## Launch Tier
- **M, Targeted**, Focused comms to the eligible heavy users, through owned channels only. No press, no events, no paid media.

It matches the goal. Conversion among a known, reachable group needs targeted messaging (in-app, push, email to the eligible list), not broad reach.
The demand is untested. The 2023 evidence is stated interest and one weak fake door. Spending on L or XL before activation is proven would risk a lot against an unvalidated assumption.
Economics are thin. By the deck’s ball-park, the card earns about 0.1% interchange where checkout earns 1.54%, so heavy launch spend is hard to recover.
The experiment needs it. An A/B test with a holdout depends on controlled, owned-channel exposure. Press, events or open social would leak the offer to control users and break the isolation.
Trust needs precision. The barriers are SCHUFA fear and doubt about who stands behind the card. Those call for clear, specific messages to the right people, not volume.

## Channels
1. **Owned: Action center (primary). This is where users already handle things in the app, and the card is set up and used there. It is the one place the offer, the trust answers and the “add to wallet” step can sit together. It is also free, and you can gate it exactly by experiment assignment.**
2. **Owned: Push notification (the trigger). Eligible users are heavy app users, so push gets them to the Action center quickly and costs almost nothing. Keep it to a short prompt that points to the offer, not a place to explain the card.**
3. **Owned: Email (the explainer). The 2023 research shows users asking who Riverty is, what the card costs, and what it means for their credit before they will commit. Email is the only one of the four with room for those answers and the legally required terms, and users can come back to it later.**

## Enablement & Assets
Must have before launch

Approved message set for the Action center, push and email, plus the legally required card terms.
Support playbook: top contacts, approved answers, escalation paths, and a “never say” list (no unapproved SCHUFA or credit claims, no launch dates, no promises of cashback).
Decline reason guide: each decline type, what the user sees, what Support says.
Return and pause rules: one page covering how a user reports a return, how long the pause lasts, and what happens if an item doesn’t come back. This needs Risk and Finance input first.
Who’s in the test: a way for Support to check whether a user is in the offered or holdout arm, and a log for contamination.
In-app help: a short FAQ linked from the Action center card covering who issues the card, what it costs, and how to add it to a wallet.

Should have
7. Merchant one-pager for CS and Sales, covering the card, what stays unchanged, and how checkout is protected.
8. Escalation and incident path: who decides to pause the offer if the guardrail trips.
9. Weekly support readout: top contact reasons, so the product team sees problems early.

Could have, later
10. Short explainer video, wider help centre articles, and merchant co-marketing, once the decision rule says ship.

## Ownership, Budget & Timeline
- **Ownership & budget:** - PM: owns the launch plan, the decision rule, post-launch metrics and
  the day-56 decision.
- Data / Analytics: owns experiment design, randomisation, A/A check,
  list freezes, and the weekly guardrail and metric reads.
- Engineering: owns wallet provisioning, confirming existing features
  work on card orders, and exposure logging.
- UX: owns the in-app Action center card, push notification design and
  the in-app FAQ.
- Marketing: owns email copy and send schedule, and works with UX on
  push copy.
- CRM: owns send logic, consent checks and channel exposure reporting.
- Legal / Compliance: owns approval of all consumer messages, card
  terms, and SCHUFA and fee wording.
- Risk / Finance: owns return and pause rules for off-network
  purchases, and guardrail boundaries including the margin threshold.
- Customer Support: owns the playbook, decline guide, return-rules
  page and the contamination log.
- Customer Success / Sales: owns the merchant one-pager and merchant
  questions.
- UX Research: owns the displacement survey.
- **Timeline:** LAUNCH AND ENROLMENT (days 0 to 14)

Day 0
- Randomise 50/50; start offer to the offered arm only.
- Action center card live; push notification sent.
- Daily support contact review begins.

Days 1 to 2
- Email: who issues the card, what it costs, how it works.

Day 5
- Single push reminder to offered users who have not activated.

Days 10 to 12
- Final email or Action center nudge; then stop.

Day 14
- Enrolment closes.
- READ 1: activation rate of offered users and exposure by channel.
- Guardrail check: checkout completion rate vs. holdout (pause rule).

OBSERVATION (days 14 to 42)

Weekly
- Guardrail read: checkout completion, on-time payments, complaints
  on SCHUFA, fees and declines, contribution margin per user.
- Support readout of top contact reasons; update FAQ.
- Log any holdout contamination.

Day 28
- Mid-point check on off-network share among activated users.

Day 42
- Last users finish 28 days of observation.
- READ 2: off-network share and displacement answers.

SETTLEMENT AND DECISION (days 42 to 56)

Days 42 to 56
- 14-day lag so returns and refunds settle.

Day 56
- READ 3: net combined Riverty volume per eligible user, offered
  vs. holdout, with guardrails.
- Decision per the pre-recorded rule: ship, extend once (28 days),
  or stop.

## Success Metrics
- **Metrics:** HOW WE'LL KNOW IT WORKED

Goal: Conversion. An eligible heavy user takes up the Riverty Card and
makes a first purchase outside the Riverty network.
All thresholds are proposals, to be agreed before launch and recorded
with the decision rule.

SUCCESS METRICS

1. Activation rate (primary, read at day 14)
   What: share of offered, eligible users who activate the card.
   Why it matches the goal: it is the conversion event itself.
   Target: at least 5% = on track; 2% to under 5% = extend;
   under 2% = stop signal (together with metric 2).
   Basis: case model implies about 3% active; 2023 fake door gave
   5% "keep me informed" (a weak signal).

2. Off-network first purchase rate (read at day 42)
   What: share of activated users who make at least one purchase at a
   merchant outside the Riverty network within 28 days of activation.
   Why it matches the goal: it shows the card is used for the job it
   was built for, not just activated.
   Target: at least 50% = on track; 10% to 49% = extend;
   under 10% with no upward trend = stop signal.
   Supporting evidence: displacement survey. At least 60% of answers
   (minimum 300) should name Klarna, PayPal or debit as the
   alternative.

3. Net combined Riverty volume per eligible user (business outcome,
   read at day 56)
   What: checkout volume plus card volume, minus refunds, per eligible
   user over 28 days, offered vs. holdout (baseline EUR 180).
   Why it matches the goal: it shows conversion translated into spend
   Riverty keeps.
   Target: about +2% (EUR 3.60), positive with the 90% interval
   excluding zero.
   Note: the likely lift is 0 to 2%, so a flat result is inconclusive
   on volume, not a clean "no".

GUARDRAIL (must hold for any success call)
- Riverty checkout completion rate at partner merchants: offered arm
  no more than 1 percentage point below the holdout.
- Also read: on-time payments, complaints on SCHUFA, fees and declines,
  and contribution margin per user.

HOW IT'S READ
- Day 14: metric 1 and the pause rule on the guardrail.
- Day 42: metric 2 and the displacement answers.
- Day 56: metric 3 and all guardrails, then the ship, extend or stop
  decision per the recorded rule.
- Analyse by assignment (all offered vs. all holdout) for metric 3.
- **Bad signal to watch for:** DO NOT JUDGE SUCCESS ON - Opens, clicks or impressions. They show reach, not conversion, and   are for diagnosing exposure only. - Total card sign-ups without activation or first off-network use. - Brand preference (6% in the brief). It is a longer-term outcome,   not a launch result.
- **Likely post-launch decision:** Iterate - Activation 2 to under 5%, or off-network use 10 to 49%, or displacement below 60%, or a positive but non-significant volume effect, with guardrails holding
