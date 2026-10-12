# A/B Experiment Brief, Riverty business-unit case

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | pay-after-you-keep invoice, delivered through the card offer to already-onboarded heavy users |
| Persona | Lena, the Decide-First Juggler: A salaried, phone-first online shopper who spreads BNPL across Klarna, PayPal and Riverty, using whichever appears at checkout, and who often orders items she may send back |
| Expected outcome | Offering the Riverty Card to eligible heavy users will raise net combined Riverty volume per eligible user by about 2% (EUR 3.60) over 28 days, because card purchases at merchants outside the Riverty network replace spend that would otherwise go to Klarna, PayPal or debit. |
| Primary success metric | Net combined Riverty volume per eligible user over 28 days: checkout volume plus card volume, minus refunds, for every eligible user in both arms. Cap extreme buyers at a high percentile, and adjust for each user’s pre-test spend to cut noise.  It exists in the control arm, it counts only money Riverty keeps, and it rises only if Lena stops sending purchases to Klarna, PayPal or her debit card. Moving a purchase from Riverty checkout to the card doesn’t change it. |
| Baseline rate | EUR 180 net combined volume per eligible user per 28 days. |
| Guardrail metric | Riverty checkout completion rate at partner merchants: completed Riverty checkout payments divided by Riverty checkout payments started, pooled across all eligible users in each arm. |
| Guardrail boundary | The offered arm’s completion rate must not be more than 1 percentage point below the holdout’s. I’ve used a one-sided test at 95% confidence. |
| Second guardrail | · |
| Minimum Detectable Effect | 2% EUR 3.60 per user |
| Sample size per arm | 31000 |
| Traffic split | 50/50 |
| Test duration | 14 day enrollment + 28-day observation, read at day 56 |
| Significance threshold | α = 0.10, two-sided, with 80% power |

## Control vs. Variant
- **Control (A):** Eligible, fully onboarded heavy app users in the holdout get no card offer and no card messaging. They keep today’s Riverty experience: Riverty checkout at partner merchants, and the existing return notifications (consumer and merchant), return pause, keep-or-return nudges, push notifications and autopay on their checkout invoices. Where Riverty isn’t offered, Lena still switches to Klarna or PayPal, or pays directly by debit card and waits for refunds on returns. Her open payments still sit across several apps with different due dates and return rules, so the moment of misery is unchanged. Measured: net combined Riverty volume (checkout only), checkout completion rate, and on-time payment rate. Card measures are empty by design.
- **Variant (B):** The one change: eligible, fully onboarded heavy app users in the offered arm get the Riverty Card, whose only mode is the pay-after-you-keep invoice. The offer, card, wallet setup and invoice ship as one unit. Card invoices use the same existing return notifications, pause, nudges, push notifications and autopay that checkout invoices already have, with no new feature built for the card. Lena can pay with the card at merchants outside the Riverty network, so nothing leaves her account at purchase. She gets one invoice per purchase, due in 14 days (placeholder), and can inspect the item first. If she reports a return, the due date pauses as it does today. Her reminders and nudges arrive as they do today, and she can set autopay for small amounts. Everything else is identical to control. Measured: the same as control, plus activation, off-network share, and the displacement question for activated users.
- **Held constant (isolation check):** Isolation check: what has not changed

The one intended difference: the offered arm can get the Riverty Card with the pay-after-you-keep invoice.

Identical in both arms:

Eligible population and rules, with the list frozen before assignment.
Riverty checkout at partner merchants, including today’s return handling.
Return notifications (consumer and merchant), return pause, keep-or-return nudges, push notifications and autopay as they exist today.
Reminder process and fee rules.
App version, channels, CCD2 rollout dates, observation window and metric definitions.
The frozen merchant list that defines “off-network”.
No new features built for either arm.

## Hypothesis
> I believe that pay-after-you-keep invoice, delivered through the card offer to already-onboarded heavy users for Lena, the Decide-First Juggler: A salaried, phone-first online shopper who spreads BNPL across Klarna, PayPal and Riverty, using whichever appears at checkout, and who often orders items she may send back will result in Offering the Riverty Card to eligible heavy users will raise net combined Riverty volume per eligible user by about 2% (EUR 3.60) over 28 days, because card purchases at merchants outside the Riverty network replace spend that would otherwise go to Klarna, PayPal or debit., as measured by a 2% EUR 3.60 per user change in Net combined Riverty volume per eligible user over 28 days: checkout volume plus card volume, minus refunds, for every eligible user in both arms. Cap extreme buyers at a high percentile, and adjust for each user’s pre-test spend to cut noise.  It exists in the control arm, it counts only money Riverty keeps, and it rises only if Lena stops sending purchases to Klarna, PayPal or her debit card. Moving a purchase from Riverty checkout to the card doesn’t change it. within 14 day enrollment + 28-day observation, read at day 56. We will protect Riverty checkout completion rate at partner merchants: completed Riverty checkout payments divided by Riverty checkout payments started, pooled across all eligible users in each arm. throughout the test.

## Shipping criteria
> We will **ship** if Net combined Riverty volume per eligible user over 28 days: checkout volume plus card volume, minus refunds, for every eligible user in both arms. Cap extreme buyers at a high percentile, and adjust for each user’s pre-test spend to cut noise.  It exists in the control arm, it counts only money Riverty keeps, and it rises only if Lena stops sending purchases to Klarna, PayPal or her debit card. Moving a purchase from Riverty checkout to the card doesn’t change it. improves by ≥ 2% EUR 3.60 per user at α = 0.10, two-sided, with 80% power and Riverty checkout completion rate at partner merchants: completed Riverty checkout payments divided by Riverty checkout payments started, pooled across all eligible users in each arm. does not reach The offered arm’s completion rate must not be more than 1 percentage point below the holdout’s. I’ve used a one-sided test at 95% confidence. after 14 day enrollment + 28-day observation, read at day 56.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 day enrollment + 28-day observation, read at day 56, no results reviewed before this date.
