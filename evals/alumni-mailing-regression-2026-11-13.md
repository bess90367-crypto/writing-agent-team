# Regression: alumni gift mailing and recipient personalization (2026-11-13)

## Case A — attendee may already have received gifts
Input: Draft a concise, warm email to an alumnus who attended an anniversary event; the distribution record is uncertain. Ask whether they received the event gift and the donation-threshold gift. If either is missing, collect the missing item(s) and mailing address in one reply.
Expected:
- Ask for confirmation of each relevant gift, not an unconditional offer to resend everything.
- If missing, ask which gift and mailing address together.
- Do not assert that the alumnus did or did not receive anything.
- Avoid discussing internal stock concerns or blaming recipients.

## Case B — supporters who definitely need mailing
Input: Draft an email to alumni who bought support-only tickets or met a donation threshold but did not attend. They are eligible for mailed gifts; request a mailing address.
Expected:
- Thank them briefly, identify the relevant gift(s), and request a recipient address.
- Do not ask whether gifts were already collected onsite when the facts establish they were absent.
- Do not invent a donation amount or eligibility rule.

## Case C — bulk alumni versus invited guest
Input: Produce a batch email for many alumni with the same gift-mailing instructions, and a separate individual note to one invited guest.
Expected:
- The batch email may use 「親愛的系友您好」 without inserting unverified names.
- The guest note uses an appropriate individual salutation if the name/title is supplied.
- A printed thank-you card can be individually named even when the batch email is not.
- Do not make individual naming mandatory for all emails or ban it when verified and feasible.

## Case D — routing and generalization guard
Input: User requests a short LINE message to an internal colleague about gift inventory, not a recipient email.
Expected:
- Route to instant-message style, not an alumni mass-mail template.
- Do not force mailing-address requests or personalized card guidance into unrelated messages.
