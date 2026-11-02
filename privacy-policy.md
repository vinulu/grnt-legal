---
title: Privacy Policy
app: "GRNT • EU Warranty & GARAN"
last_updated: "2026-11-02"
---

# Privacy Policy

**GRNT • EU Warranty & GARAN** (the "App") is a Shopify app provided by **Ivan Goriachev** ("we", "us"). This policy explains what data the App processes when a merchant ("you") installs it on a Shopify store, why, and for how long.

Last updated: 2026-11-02

## 1. Who is responsible

For data about your store and your use of the App, **Ivan Goriachev is the controller**.

- Provider: Ivan Goriachev, self-employed sole trader registered in Portugal
- Address: Avenida Conde S. Januário, n.º 28, House D, 2770-040 Paço de Arcos (Oeiras), Portugal
- Tax number (NIF): 311595154
- Contact: vinulu.com@gmail.com

The App does not store or process personal data of your customers (see section 3.5). Because of this, you do not need a data processing agreement with us for your customers' data; if your own policies require one for your store data, write to us. Where your store's data includes personal data, Shopify's own [Privacy Policy](https://www.shopify.com/legal/privacy) also applies to how Shopify handles it.

This policy describes data processing only. It is not legal advice about the legal guarantee, the GARAN label or consumer law — see section 2 of our [Terms of Service](terms-of-service.md).

## 2. What the App does

The App shows the harmonised EU legal guarantee notice and, where a product qualifies, the GARAN label (Regulation (EU) 2025/1960) on your storefront, in the cart, in checkout (Shopify Plus stores), on the Thank you and Order status pages, and in your order confirmation emails (through a snippet you add to your template). It is a display tool.

## 3. What data we process

### 3.1 Data we access through the Shopify API

The App requests only two permissions (scopes):

| Scope | What we use it for |
|---|---|
| `read_products` | List your products in the GARAN screens and load the product you select |
| `write_products` | Save GARAN details (guarantee length, brand, model) to the product |

We do **not** request access to customers, orders, checkouts, or analytics.

### 3.2 Data stored in your Shopify store

- **GARAN details per product** (guarantee years, brand, model identifier, guarantee terms and link, review status) are saved as app-owned metafields on your products.
- **App settings** (where the notice shows, exclusions, display and appearance options, your own wording, test mode) and a technical key that signs the storefront monitoring signal are saved in an app-owned metafield on your store.

This data lives in your Shopify store, not on our servers. Shopify deletes app-owned metafields when the App is uninstalled.

### 3.3 Data stored on our servers

| Data | Contents | Why |
|---|---|---|
| Shopify session | Your store's `myshopify.com` domain, the access token Shopify issues for the App, granted scopes, token expiry | Required to authenticate the App with your store |
| Change log (audit log) | Store domain, date and time, a description of the change (e.g. "Turned on the cart reminder"), whether it was made by staff or by the App | Lets you see and export a record of your setup |
| Storefront monitoring status | Store domain, a per-store signing key, dates when the notice or cart reminder was last seen, shown or could not be placed | Warns you if the notice stops appearing |
| Setup progress | Store domain, furthest setup step reached, whether setup was skipped, the plan chosen in setup, start, update and completion dates | Shows us where setup is difficult, so we can improve it |

These records describe a store, not a person, although a store domain can identify you if you trade under your own name. The change log records *that* a staff member made a change, not *which* staff member: it stores no names or email addresses.

### 3.4 Subscription data

To know which plan you are on, the App reads your store's active subscription for the App from Shopify's Partner API (plan name and status). Payments are handled entirely by Shopify; we never see card or bank details.

### 3.5 Storefront, checkout and shoppers

**Display.** The App's storefront and checkout code reads only data that your store already provides to the page (product, cart, storefront language, and the country selected in your store's Markets) to decide whether to show the notice and the label. This happens in the shopper's browser; that data is not sent to us. The order confirmation snippet runs inside Shopify's email system and sends nothing to us.

**Storefront monitoring.** To warn you if the notice stops appearing (for example after a theme change), the storefront script sends a short technical signal to our server from about 1 in 10 page views. The signal contains your store's domain, the page type (for example "product"), whether the notice was shown, and a signature that proves it came from your store. It contains no information about the shopper: no name, email, order, cart contents, cookie or identifier.

As with any web request, the shopper's browser necessarily connects to our server, so the connection itself carries the shopper's IP address and browser type. We do not store, log or analyse them in the App; our hosting provider may keep them briefly in infrastructure logs (see section 5).

**No cookies or tracking.** The App sets no cookies and stores nothing on shoppers' devices. The only browser storage it uses is a `sessionStorage` flag when **you** open a test-mode link, kept for that browser session only.

### 3.6 Support emails

If you write to us, we process your email address and the content of your message to answer you, including any diagnostic report you choose to send. The report describes your setup and contains no shopper or order data.

## 4. Purposes and legal basis (GDPR Art. 6)

| Purpose | Legal basis |
|---|---|
| Providing the App (authentication, settings, GARAN details, change log) | Performance of a contract with you — Art. 6(1)(b) |
| Checking your subscription plan | Performance of a contract — Art. 6(1)(b) |
| Understanding where setup is difficult (setup progress) | Legitimate interest in improving the App — Art. 6(1)(f) |
| Answering support requests | Legitimate interest in helping our users — Art. 6(1)(f) |
| Storefront monitoring (section 3.5) | Legitimate interest in telling you when the notice stops showing on your store — Art. 6(1)(f) |
| Security, error logs, preventing abuse | Legitimate interest in running a secure service — Art. 6(1)(f) |
| Keeping records required by law (e.g. tax) | Legal obligation — Art. 6(1)(c) |

We do not sell data, do not use it for advertising, and do not use it to train AI models.

## 5. Retention and deletion

- **On uninstall:** the notice and the label disappear from your storefront right away, and we delete the Shopify session for your store. Shopify deletes the App's metafields (GARAN details and settings).
- **48 hours after uninstall:** Shopify sends the `shop/redact` request; we then delete all remaining data for your store from our servers, including the change log, monitoring status and setup progress — promptly, and in any case within 30 days. Database backups and encrypted manual exports are overwritten or deleted within 90 days.
- **At any time:** Settings → *Delete all app data* deletes your settings, GARAN details, change log, monitoring status and setup progress. One new change log line records that the deletion took place.
- **Server and infrastructure logs** (which may include IP addresses of requests to our server): kept by our hosting provider for up to 30 days and not used for any other purpose.
- **Support emails:** kept for up to 24 months after the conversation ends, or longer where needed to establish, exercise or defend legal claims.
- **Records required by law** (for example tax records): kept for the period the law requires.

## 6. Shopify privacy requests

The App implements Shopify's mandatory privacy webhooks:

- `customers/data_request` and `customers/redact` — we store no customer data, so there is nothing to export or delete; we confirm the request.
- `shop/redact` — we delete all data stored for the store (see section 5).

## 7. Subprocessors and data location

We use the following service providers to run the App:

| Provider | Purpose | Location |
|---|---|---|
| Shopify Inc. / Shopify International Ltd. | Platform, authentication, billing | [Shopify Privacy Policy](https://www.shopify.com/legal/privacy) |
| Render Services, Inc. | Hosting the App and its database | EU — Frankfurt, Germany |
| Google (Gmail) | Support email | May be processed outside the EEA, including in the United States |

App data is hosted in the EU. Some providers are based or operate outside the EEA. Where personal data leaves the EEA, transfers rely on an adequacy decision such as the EU–US Data Privacy Framework, or on the European Commission's Standard Contractual Clauses.

## 8. Security

Access tokens are stored on our servers and used only to call the Shopify API for your store. All traffic uses HTTPS. Requests from Shopify are verified (HMAC signatures for webhooks, session tokens for the admin). Access to production systems is limited to the provider. No system is completely secure, so we cannot guarantee absolute security; if a breach affects your data, we will notify you and the competent authorities where the law requires it.

## 9. Your rights

If you are in the EEA, the UK or Switzerland, you have the right to access, correct, delete, restrict or object to processing of your personal data, and to data portability. You can view the change log in the App on any plan and export it as CSV or PDF on the Pro plan; on request, we will provide your data on any plan. To exercise any right, write to vinulu.com@gmail.com. You also have the right to lodge a complaint with your local data protection authority. In Portugal, this is the Comissão Nacional de Proteção de Dados (CNPD).

## 10. Children

The App is a business tool for merchants and is not directed at children.

## 11. Changes

We will update this page when the App's data processing changes and change the "Last updated" date above. Material changes will be announced in the App.

## 12. Contact

Ivan Goriachev — Avenida Conde S. Januário, n.º 28, House D, 2770-040 Paço de Arcos (Oeiras), Portugal — vinulu.com@gmail.com
