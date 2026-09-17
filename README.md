# Northline Web Works

Northline Web Works is a small-business digital services storefront and private project desk.

## What it includes

- Public service catalog for writing, presentations, spreadsheets, and one-page websites
- Free project-request form with rate limiting and spam protection
- Automatic owner alert and customer confirmation email support through Resend
- Private owner-only Studio Desk for reviewing requests and tracking status
- Stripe-hosted payment-link workflow so card details never pass through this app
- Private project payment pages
- Google Search Console verification, sitemap, robots rules, and SEO metadata
- Responsive mobile/desktop design
- D1-backed request storage

## Customer flow

1. A customer submits a free request.
2. The request is saved before email delivery is attempted.
3. Northline Web Works receives an owner alert when email is configured.
4. The customer receives an automatic confirmation and a 2–3 business day response expectation.
5. Scope, final price, deadline, and terms are agreed before payment.
6. The eligible merchant-account owner creates a Stripe payment link.
7. Work is reviewed and delivered by the studio.

## Development

Requires Node.js 22.13+ and pnpm 11.25.0.

```bash
pnpm install
pnpm lint
node tests/email.test.mjs
pnpm build
```

The hosted production site uses Cloudflare/Vinext bindings declared in `.openai/hosting.json`.

## Safety and privacy

Do not place passwords, card numbers, private API keys, or customer secrets in the repository. Payment processing is handled by Stripe-hosted checkout. Project briefs should not contain sensitive personal or financial information.
