# RWANDA GLOBAL MARKET

A zero-budget, static-first MVP for global product discovery, affiliate referrals and sourcing enquiries.

## Important launch status
This is a deployable **starter storefront**, not an active Alibaba integration. Sample catalogue items are illustrative. No live inventory, price, order, payment, shipment or affiliate tracking is claimed. Add only your own approved Alibaba tracked URLs after your affiliate application is accepted.

## 1. Configure the site
Edit `config.js`:
- Set `contactEmail` to an inbox you control.
- Optionally set `whatsappNumber` to an international number without `+`.
- Replace sample product records with real offers you are allowed to promote.
- Paste each unique affiliate tracking URL into that product's `affiliateUrl`.

Never put an Alibaba App Secret, access token, bank details or other private credential in `config.js`. It is public browser code.

## 2. Run locally
No build step is required. Open `index.html` in a browser, or run a local static server:
```bash
npx serve .
```

## 3. Deploy for free
### Netlify
1. Push this folder to a GitHub repository.
2. In Netlify choose **Add new site → Import an existing project**.
3. Select the repository.
4. Build command: leave blank.
5. Publish directory: `.`.
6. Deploy.

### Vercel
1. Import the GitHub repository in Vercel.
2. Framework preset: Other.
3. Build command: leave blank.
4. Output directory: `.`.
5. Deploy.

A free subdomain is available on these platforms; a custom domain usually costs money.

## 4. Alibaba affiliate onboarding
Use the individual registration route at https://ads.alibaba.com/?src=influenceaffiliate.
Follow Alibaba's official help instructions:
- Register as an individual using your legal name.
- Choose Publisher / Network.
- Verify your email and complete your profile.
- Add your website or other media.
- Submit the Event Promotion agreement for approval.
- After approval, obtain your affiliate tracking links in the portal and add them to `config.js`.

Official help: https://ads.alibaba.com/help/register.htm
Affiliate portal: https://ads.alibaba.com/

## 5. API integration — approval required
Alibaba.com Open Platform onboarding describes developer registration, application review, App Key/App Secret issuance and separate API permission requests:
https://openapi.alibaba.com/doc/doc.htm?docId=118729&nodeId=27493

Do not assume the affiliate portal grants Open Platform API access. They are separate approval paths. This MVP deliberately does not invent endpoints or credentials. Add an API only after Alibaba confirms the specific product/API, permitted use, rate limits, signature/authentication method and commercial terms in your developer console.

## 6. Current limitations
- The sourcing form prepares an email using the visitor's email application. It does not store or send enquiries on a server.
- Product links are manually configured affiliate URLs, not API-synced listings.
- No checkout, payment processing, inventory, customer accounts or shipment booking is implemented.
- No backend is included, so do not collect sensitive personal or payment information.
- Affiliate disclosure is displayed in the footer. Keep it visible and comply with Alibaba's current agreement and local laws.

## Recommended next phase
After affiliate approval: add a server-side integration only if Alibaba provides an approved API suitable for affiliate product feeds. For real sourcing orders, establish supplier verification, written quotations, shipping/customs process, payment provider, refunds and customer support before accepting money.
