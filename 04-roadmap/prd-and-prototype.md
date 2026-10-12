# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** Pay-after-you-keep invoice. Creates a per-purchase invoice with a due date, so money leaves her account only after she has decided to keep the item.
- **My finalized Must-Haves (after overriding the AI):** MUST HAVE
One invoice per cleared card purchase, in Riverty. It carries the merchant, final amount, purchase date and due date. This is the core promise, and a monthly bundle breaks "decide per purchase".
No debit at purchase. Her bank account is charged only when she pays the invoice. This is the "money leaves only after I've decided" requirement.
Fixed due date set at creation. It is a configuration value that Risk and Finance sign off, not user-selectable. Without a date she can't decide or plan.
Real-time approval at authorisation. A fraud check, a solvency check and a cap against her approved limit. No approval means no purchase and no invoice.
Invoice from the final cleared amount. Reversed or expired authorisations create no invoice, so she is never billed for a purchase that didn't complete.
Invoice detail screen with a Pay action. She sees merchant, amount, due date and status, and pays through Riverty's existing invoice payment flow, with no new collection mechanism. Without it she can't see or settle what she owes.
No interest or fee if paid by the due date. This is a pricing rule, not a build. Charging for the "decide first" window would defeat the promise.
- **What I demoted from Must → Should/Won’t, and why:** -

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** All the Unhappy paths and edge cases.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** It didn't give me a view of all the invoices. That's something I would add.
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** https://claude.ai/artifact/KTtfDe4jRUV7ZSmjyPdf9y
