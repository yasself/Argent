# Global banking & payments access for a Morocco-resident founder (state at 12 Nov 2026)

Scope: (a) Moroccan company / Moroccan-resident sole proprietor; (b) foreign company (US LLC/C-Corp, UK Ltd, Estonian OÜ, UAE free-zone, HK/SG) whose sole owner-director is a Moroccan national residing in Morocco.

Source labels used on every line: **[O]** = official provider page read directly on 2026-11-12; **[O-snippet]** = official page seen only through a search-result excerpt (page itself returned 403/404); **[S]** = secondary (press, vendor blog, comparison site); **[A]** = anecdotal (forum/user reports). All URLs accessed 2026-11-12 unless another date is given.

Compliance note: nothing below assumes misdeclaring residence, borrowed identities, or VPN/address tricks. Where a provider gates on the owner's residence or ID-issuing country, the honest answer for a Morocco resident is recorded as "blocked".

---

## 1. Summary matrix (who is actually reachable)

### Takeaway
For a Moroccan entity (a), the realistically open doors are: merchant-of-record platforms that list Morocco (Paddle, Lemon Squeezy docs, Creem, probably Whop), Payoneer, a limited PayPal, local CMI/aggregator acquiring settling in MAD, and SWIFT into a Moroccan bank; Stripe, Stripe Managed Payments, Polar, Dodo (since March 2026), Google Play merchant and AWS Marketplace paid listings are closed. For a foreign company (b), the entity country opens Stripe / Managed Payments / AWS / Google Play, and Mercury and Relay do not list Morocco as a prohibited owner country, but several providers gate on the owner's residence or ID country (Dodo explicitly, Revolut Business, Wio/UAE banks, Novo/Brex by secondary reports).

### Cited Findings

Matrix A — Payment processing / MoR

| Provider | (a) Moroccan entity / resident | (b) Foreign co., owner resident in Morocco | Payout route to Morocco | Fees found | Source type |
|---|---|---|---|---|---|
| Stripe (direct account) | No. Morocco not among the 51 listed countries/regions | Yes at entity level if entity is in a listed country (US, UK, EE, AE, HK, SG all listed) | N/A (payout goes to the entity's bank in the entity's country) | not re-verified here | [O] [stripe.com/global](https://stripe.com/global) |
| Stripe Managed Payments (MoR) | No. Supported business locations: US, CA, 31 European countries incl. EE and GB, AU, HK, JP, SG | Yes for US/UK/EE/HK/SG entities subject to "eligibility review that considers business type and geography"; UAE not listed | via entity's Stripe account | fee not on page read | [O] [Stripe docs – eligibility](https://docs.stripe.com/payments/managed-payments/eligibility) |
| Stripe Global Payouts to Morocco | Receive-only: a US/UK Stripe platform can pay a Moroccan recipient (individual or company) in MAD by "local bank method"; required info = email + name/company name | n/a | MAD to Moroccan bank account | not on page read | [O] [recipient requirements](https://docs.stripe.com/global-payouts/recipient-requirements), [changelog 2025-12-15](https://docs.stripe.com/changelog/clover/2025-12-15/cross-border-payouts-new-countries) |
| Paddle | Accepted in principle: Morocco is not on the unsupported-country list (list "subject to change") | Accepted | not verified (payout page 404) | not verified | [O] [Paddle supported countries](https://www.paddle.com/help/start/intro-to-paddle/which-countries-are-supported-by-paddle) |
| Lemon Squeezy | Docs list Morocco under bank payouts; product in "transition" to Stripe Managed Payments, no shutdown date, slower support | Same | Bank payout (Morocco listed); PayPal "200+ countries" | not verified | [O] [LS supported countries](https://docs.lemonsqueezy.com/help/getting-started/supported-countries), [LS 2026 update](https://www.lemonsqueezy.com/blog/2026-update) |
| Polar | No: Morocco absent from payout list (Stripe Connect Express) | Yes if entity is in a listed country | — | not on page | [O] [Polar supported countries](https://polar.sh/docs/merchant-of-record/supported-countries) |
| Dodo Payments | No for new merchants: Morocco is only in the "grandfathered" group (merchants served before the 23 Mar 2026 policy) | Blocked in practice: "if a director or beneficial owner can only verify with an ID issued in a country that is not listed", the account cannot be onboarded | — | — | [O] [Dodo accepted countries](https://docs.dodopayments.com/miscellaneous/accepted-countries-and-territories) |
| Creem | Yes: Morocco in the 87 supported merchant/payout countries, no restriction marker | Yes | Local bank transfer | payout fee = greater of 7 EUR/USD or 1% | [O] [Creem supported countries](https://docs.creem.io/merchant-of-record/supported-countries) |
| Whop | Probably: payouts to bank / mobile wallet / crypto wallet in "over 200 countries"; Morocco not named, not seen on sanctions list | Yes | bank (crypto option must be excluded for Morocco, see §8) | not verified | [O-snippet] [Whop payout methods](https://docs.whop.com/manage-your-business/manage-payouts/payout-methods) |
| 2Checkout / Verifone | Unverified country eligibility | Unverified | wire (15 USD/GBP/EUR fee on 2Sell/2Subscribe), PayPal, Payoneer; "payouts not available in restricted countries" | wire fee 15 | [O-snippet] [2Checkout payouts](https://docs.2checkout.com/get-started/getting-started/payouts) |
| Gumroad | Unverified (help pages did not render) | Unverified | PayPal fallback where bank payouts unsupported (help-page excerpt) | — | [O-snippet] [Gumroad getting paid](https://gumroad.com/help/article/13-getting-paid) |
| FastSpring, PayPro Global | No data found | No data found | — | — | gap |
| Adyen | Not practical: unpublished minimum invoice; reviewers cite ~USD 120/month or EUR 100/month | same | — | — | [S] [costbench](https://costbench.com/compare/adyen-vs-checkout-com/) |
| Checkout.com | Not practical: third-party claim of USD 50–100k/month minimum volume | same | — | — | [S] [costbench](https://costbench.com/compare/adyen-vs-checkout-com/) |
| PayPal (Morocco account) | Limited; since Sept 2025 PayPal balance can be withdrawn to MAD in the Cash Plus app (~30 MAD/operation) | n/a | Cash Plus wallet; Moroccan bank (third-party-cited fee: free above 2,000 MAD, 30 MAD below) | — | [S] [Médias24 16/09/2025](https://medias24.com/2025/09/16/cashplus-lance-via-son-application-le-retrait-des-soldes-paypal-en-mad/), [Grey](https://grey.co/blog/how-to-withdraw-paypal-funds-in-morocco) |
| PayPal (US LLC, foreign owner) | n/a | Uncertain: guides conflict on whether SSN/ITIN is mandatory; verification described as strict | — | — | [S] [businessanywhere](https://businessanywhere.io/stripe-paypal-non-resident-us-llcs-what-to-know/), [doola help](https://help.doola.com/how-to-set-up-a-u.s.-paypal-account-under-an-llc-itin-requirements) |

Matrix B — Banking / EMI

| Provider | (a) Moroccan entity / resident | (b) Foreign co., owner resident in Morocco | Fees found | Source type |
|---|---|---|---|---|
| Mercury (US) | No (US entities only) | Likely yes: Morocco is not in the restricted list reproduced by doola (updated 30 Oct 2026); Mercury cannot mail physical cards to Morocco | not verified | [S] [doola Morocco guide](https://www.doola.com/mercury-guide/how-to-open-a-mercury-account-in-morocco/); [O-snippet] [Mercury card restrictions](https://support.mercury.com/hc/en-us/articles/34087163095572) |
| Relay (US) | No | Yes on paper: non-US owners accepted; prohibited list (citizenship or residency of any owner) does not include Morocco; updated 11 Aug 2026 | not verified | [O] [Relay prohibited countries](https://relayfi.com/hc/en-us/articles/10239600121748-Prohibited-Countries/) |
| Bluevine (US) | No | Conflicting: Bluevine blog says non-residents with a US entity can apply; a 2026 comparison says it effectively requires a US-person owner | — | [O-snippet] [Bluevine blog](https://www.bluevine.com/blog/introducing-bluevine-for-international-business-owners); [S] [globalsolo](https://www.globalsolo.global/blog/mercury-vs-wise-vs-relay-best-bank-2026) |
| Novo (US) | No | Mostly no: reported to require SSN for all beneficial owners (one source says passport/ITIN possible) | — | [S] [beancount.io 6 Oct 2026](https://beancount.io/blog/2026/10/06/us-business-banking-without-us-address-nonresident-founders-guide) |
| Brex (US) | No | Reported no for non-US residents without US presence/funding; acquired by Capital One in April 2026 per one source | — | [S] [beancount.io](https://beancount.io/blog/2026/10/06/us-business-banking-without-us-address-nonresident-founders-guide) |
| Wise Business | Reported not available for Morocco-registered businesses; personal accounts in Morocco described as limited/send-only, no cards | Unverified for foreign entity with Morocco-resident director; Wise rule: if business address and trading address are in different countries, only services available in both are offered | — | [S] [WorldFirst, checked Aug 2026](https://www.worldfirst.com/af/blog/business-banking-insights/wise-alternatives-africa/); [O-snippet] [Wise verify your business](https://transferwise.com/help/a/2769792/verify-your-business) |
| Payoneer | Yes (Morocco among 190+ countries per secondary source) | Yes (entity-level) | receiving account free in local currency / 1% non-local; card payer up to 3.99% + 0.49 USD; ACH/bank debit 1%; withdrawal to bank 1.2–4% (non-local or converted), 1.50 USD same-country local; balance-to-balance FX 0.5%; annual fee 29.95 USD if < 6,000 USD received in 12 months | [O] [Payoneer pricing](https://www.payoneer.com/pricing/); [S] [WorldFirst](https://www.worldfirst.com/af/blog/online-sellers/marketplace-payment-solutions/) |
| Airwallex | No evidence Morocco is a supported registration country | Entity must be registered in a supported country; article states no residence/nationality restriction for directors/UBOs; approval not guaranteed | — | [O] [Airwallex eligibility](https://help.airwallex.com/hc/en-gb/articles/900001757026-Can-I-open-an-account-with-Airwallex-) |
| Revolut Business | No | Likely blocked: company must be registered with physical presence in a supported country and the applicant must live in a supported country | — | [O-snippet] [Revolut help](https://help.revolut.com/business/help/setting-up-an-account/is-my-business-eligible/what-country-of-residence-is-eligible-to-open-a-revolut-business-account/) |
| Wio Business (UAE) | No | Likely blocked without UAE residency: third-party sources say signatory must be UAE resident with Emirates ID; Wio FAQ says accounts are for UAE-based companies with a trade licence | Essential plan 99 AED/month, no minimum balance (third-party, 18 Jun 2026) | [O-snippet] [Wio support](https://wio.io/support/); [S] [businessbankindex](https://businessbankindex.pages.dev/ae/for-saas), [wiki.private.law](https://wiki.private.law/en/wio-bank) |
| Emirates NBD / Mashreq / RAKBANK etc. | No | Selective, case by case; Meydan Free Zone states non-resident founders cannot activate a UAE corporate account without first becoming resident | Mashreq NeoBiz AED 50,000 average balance figure seen but unreliable | [S] [businessdubai.ae](https://www.businessdubai.ae/blogs/uae-bank-account-non-residents), [binderr](https://binderr.com/marketplace/ae/opening-a-business-bank-account-in-uae-for-non-residents) |
| Estonian banks (LHV etc.) for OÜ | n/a | Hard: e-Residency does not guarantee an account; <30% of ~20,000 active e-resident companies hold a traditional Estonian bank account; due-diligence fees EUR 300–750 cited | — | [O] [e-resident.gov.ee blog](https://www.e-resident.gov.ee/blog/posts/how-e-residents-can-avoid-common-business-account-mistakes/); [S] [enty.io](https://enty.io/blog/open-estonian-business-bank-account-without-visiting-2026) |
| Statrys, Currenxie, Aspire, Wamo, Zen, Wallester | No data found | No data found | — | gap |
| Moroccan bank (foreign-currency / convertible account) | Yes | n/a | see §5 | [S] |

### Inferences
- The only "MoR + Morocco entity" combinations confirmed on an official page read today are Paddle (by absence from exclusion list), Lemon Squeezy (docs list) and Creem (explicit list). Paddle and Lemon Squeezy both run their own acceptance review, so listing is necessary, not sufficient.
- Dodo's rule (ID must be issued in a listed country) is the clearest written example of a provider looking through the entity to the owner; a US LLC does not fix it.
- For structure (b), the US LLC has the widest confirmed banking access for a Morocco resident (Relay official list; Mercury by secondary list), while UAE and Revolut-type options hinge on residency the founder does not have.

### Gaps
- Mercury's own "Prohibited countries" page returned HTTP 403; Morocco's absence rests on a third-party reproduction (doola) and should be re-checked on [support.mercury.com](https://support.mercury.com/hc/en-us/articles/35628854440468-Prohibited-countries).
- Wise has no official page I could read that states Morocco's status for business or personal balances; [which countries](https://wise.com/help/articles/2978049/which-countries-can-i-use-wise-in) and [why can't I open a balance](https://wise.com/help/articles/2813542/why-cant-i-open-a-balance) do not mention Morocco.
- No data for FastSpring, PayPro Global, Statrys, Currenxie, Aspire, Wamo, Zen, Wallester, Fatourati, NAPS.
- Fees for Stripe, Paddle, Lemon Squeezy, Polar, Mercury, Relay were not re-verified in this pass.

---

## 2. Stripe: what a Morocco resident can and cannot do

### Takeaway
Stripe does not open accounts for Moroccan businesses; what launched in the 2025-12-15 API preview is Morocco as a *recipient* country for Global Payouts (a US/UK Stripe user pays a Moroccan bank account in MAD), which is not card acceptance. A foreign entity in a Stripe country can get a normal Stripe account and, for US/UK/EE/HK/SG, apply for Managed Payments.

### Cited Findings
- Stripe's country page lists 51 countries/regions (incl. US, UK, Estonia, UAE, Hong Kong, Singapore); Morocco is not listed; five African markets are "extended network" via Paystack; India and Indonesia are "preview". [O] — [stripe.com/global](https://stripe.com/global)
- Stripe Atlas is described as "Incorporate a US company from anywhere in the world". [O] — [stripe.com/global](https://stripe.com/global)
- Changelog 2025-12-15 (preview API): Global Payouts added 13 recipient countries including `ma_bank_account` (Morocco), enabling recipients to "create bank accounts and receive cross-border payouts" via Outbound Payments / Accounts v2. [O] — [Stripe changelog](https://docs.stripe.com/changelog/clover/2025-12-15/cross-border-payouts-new-countries)
- Recipient requirements table: Morocco (MA), currency MAD, "Local bank method", required info email + name (individual) or company name; listed for US and UK senders. [O] — [Stripe recipient requirements](https://docs.stripe.com/global-payouts/recipient-requirements)
- Classic Connect cross-border payouts are limited to platforms and connected accounts in US, UK, EEA, Canada, Switzerland; other destinations require Global Payouts or sales contact. [O] — [Connect cross-border payouts](https://docs.stripe.com/connect/cross-border-payouts)
- Stablecoin payouts (USDC/OUSD) exist for US senders to wallets in supported countries (public preview). [O] — [Stripe recipient requirements](https://docs.stripe.com/global-payouts/recipient-requirements)
- Managed Payments: Stripe is merchant of record; handles sales tax/VAT/GST in 80+ countries, fraud, disputes, transaction support; only Checkout and Payment Links; no Connect, no Elements, subscriptions only created through Checkout/Payment Links. [O] — [Managed Payments](https://docs.stripe.com/payments/managed-payments)
- Managed Payments eligibility: supported business locations US, CA, AT, BE, BG, CH, CY, CZ, DE, DK, EE, ES, FI, FR, GB, GR, HR, HU, IE, IT, LI, LT, LU, LV, MT, NL, NO, PL, PT, RO, SE, SI, SK, AU, HK, JP, SG; digital products only (SaaS, AI-as-a-service tax codes included, software, courses, digital media); professional services and anything with human intervention excluded; requires low historical dispute rate; Stripe may refund within 60 days. [O] — [Managed Payments eligibility](https://docs.stripe.com/payments/managed-payments/eligibility)
- Lemon Squeezy's CEO wrote on 28 Jan 2026 that Managed Payments covered merchants in 35+ countries and was waitlist-only at that time. [O] — [Lemon Squeezy 2026 update](https://www.lemonsqueezy.com/blog/2026-update)
- US Stripe account for a non-US founder: secondary guides agree a US entity + EIN are needed and that a non-resident without SSN/ITIN must obtain the EIN via Form SS-4 by fax/mail/phone; they conflict on whether an ITIN is needed for the owner (several say Stripe accepts passport/foreign ID for a non-US owner; a doola post quotes Stripe saying a US tax ID is needed for a US account). [S] — [Stripe resource on EIN from abroad](https://stripe.com/in/resources/more/how-to-get-an-ein-or-a-tin-while-living-outside-the-us), [doola](https://doola.com/blog/how-to-create-a-us-stripe-account), [terms.law](https://terms.law/Invest-USA/bank-compliance/stripe-for-foreign-llc.html)
- Stripe offers restricted API keys with per-resource scopes, IP allowlisting, expiry and rotation, and lets a key be tagged as an agent key; Stripe docs ship an "agent skills" quickstart (`stripe agent setup`). [O-snippet]/[O] — [Stripe API keys](https://docs.stripe.com/keys/customize-api-key-permissions), [Stripe docs header](https://docs.stripe.com/payments/managed-payments)
- Stripe may automatically limit an API key unused for money-movement operations for 180 days. [O-snippet] — [Stripe support](https://support.stripe.com/questions/why-does-my-api-key-have-limited-access)

### Inferences
- "Stripe payouts to Morocco" means a Moroccan person or company can be the *payee* of a platform/marketplace built on Stripe by someone in the US or UK; it does not let a Moroccan business charge cards on Stripe.
- A founder's own US LLC with a US Stripe account could in principle use Global Payouts to pay a Moroccan bank account in MAD, but whether paying one's own owner this way is permitted, and the fee, were not verified.
- A US LLC, UK Ltd, Estonian OÜ, HK or SG company owned by a Morocco resident is geographically eligible for Managed Payments; a UAE free-zone company is eligible for Stripe but not for Managed Payments.

### Gaps
- Stripe's official support article on non-US-resident requirements returned 404; no official text found on how Stripe treats owners residing in unsupported countries.
- Global Payouts fees and per-payout limits for MAD not captured (one snippet cites a 9,999,999.99 MAD max for UK senders on [payout methods](https://docs.stripe.com/global-payouts/payout-methods)).
- Whether the Morocco destination is still preview or GA in November 2026 not confirmed.

---

## 3. Merchant-of-record platforms and PayPal for a Morocco-based seller

### Takeaway
Morocco is officially listed or not excluded at Paddle, Lemon Squeezy and Creem; it is excluded at Stripe Managed Payments, Polar and (for new merchants since 23 March 2026) Dodo Payments. Lemon Squeezy is in an acknowledged wind-down-style transition toward Stripe Managed Payments, which does not accept Moroccan businesses.

### Cited Findings
- Paddle: sellers "anywhere in the world" except a list of 28 unsupported countries/regions (e.g. Iran, Libya, Mali, Russia, Zimbabwe); Morocco is not on it. [O] — [Paddle](https://www.paddle.com/help/start/intro-to-paddle/which-countries-are-supported-by-paddle)
- Lemon Squeezy: Morocco appears in the bank-payout country list; PayPal payouts in "200+ countries and regions". [O] — [Lemon Squeezy docs](https://docs.lemonsqueezy.com/help/getting-started/supported-countries)
- Lemon Squeezy, 28 Jan 2026: team focus moved to Stripe Managed Payments, causing "slower support responses and less frequent product updates"; goal is an easy migration path; no steps, deadline or statement on new-store onboarding. [O] — [Lemon Squeezy 2026 update](https://www.lemonsqueezy.com/blog/2026-update)
- Third-party reports: Managed Payments public preview Feb 2026, GA April 2026; Lemon Squeezy's site footer now reads "Sold through Link, LLC f/k/a Lemon Squeezy LLC". [S] — [Dodo blog](https://dodopayments.com/blogs/lemonsqueezy-alternatives), [issoh.co.jp](https://www.issoh.co.jp/md/tech/18599)
- Polar: payouts via Stripe Connect Express to listed countries; alphabetical list runs "Mexico, Moldova, Monaco, Mongolia, Mozambique, Namibia" with no Morocco. [O] — [Polar](https://polar.sh/docs/merchant-of-record/supported-countries.md)
- Dodo Payments: Morocco is not on the accepted list; it sits in a grandfathered group for merchants served before the 23 March 2026 policy ("may continue transacting under enhanced monitoring"); "Merchant accounts are supported only where KYC documentation is issued in the countries listed above"; registering a company in a supported country does not by itself confer eligibility. [O] — [Dodo docs](https://docs.dodopayments.com/miscellaneous/accepted-countries-and-territories)
- Dodo's own marketing pages still advertise "Merchant of Record in Morocco" and "Accept payments in Morocco". [S, contradicted by the official docs above] — [Dodo blog](https://dodopayments.com/blogs/merchant-of-record-morocco)
- Creem: Morocco in supported merchant/payout list; local bank transfer available in all 87 supported countries; payout fee greater of 7 EUR/USD or 1%. [O] — [Creem](https://docs.creem.io/merchant-of-record/supported-countries)
- Whop: payouts to bank account, mobile wallet or crypto wallet in over 200 countries. [O-snippet] — [Whop](https://docs.whop.com/manage-your-business/manage-payouts/payout-methods)
- Freemius lists Morocco among its payout countries and notes Payoneer publishes no public country list. [O-snippet] — [Freemius](https://freemius.com/help/documentation/selling-with-freemius/supported-countries)
- PayPal Morocco: since 16 Sept 2025 the Cash Plus app allows instant withdrawal of a PayPal balance in MAD, user chooses amount, about 30 MAD per operation. [S] — [Médias24](https://medias24.com/2025/09/16/cashplus-lance-via-son-application-le-retrait-des-soldes-paypal-en-mad/)
- Médias24 reports Cash Plus's explanation that a PayPal account is treated as a foreign account, which Moroccan residents are not allowed to hold; hence the repatriation mechanism. [S] — [Médias24 18/09/2025](https://medias24.com/2025/09/18/ce-que-change-concretement-le-partenariat-cash-plus-paypal-pour-les-e-commercants-et-freelances-marocains/)
- Cash Plus payment-account tiers cited at launch: 200 MAD, 5,000 MAD, 20,000 MAD ceilings. [S] — [FNH](https://www.fnh.ma/article/actualites-marocaines/cash-plus-possibilite-d-ouvrir-un-compte-de-paiement-via-agence-ou-mobile-gratuitement)

### Inferences
- A Moroccan company wanting an MoR today should treat Paddle and Creem as the primary candidates and Lemon Squeezy as a legacy option with migration risk, because its stated successor excludes Morocco.
- Payoneer is the common payout rail when a platform does not wire to Morocco (2Checkout, Fiverr, Upwork, Udemy all reference it).

### Gaps
- Paddle payout methods/currencies/threshold pages returned 404; whether Paddle wires USD/EUR to a Moroccan bank or needs Payoneer was not confirmed.
- No confirmation that Lemon Squeezy still approves new Moroccan stores in late 2026.
- Morocco PayPal business-account receiving limits not found on an official PayPal page.
- Reserve/holding policies of each MoR not captured.

---

## 4. Banks and EMIs for a foreign company owned by a Morocco resident

### Takeaway
On written policy, Relay (official list, Aug 2026) and Mercury (secondary list, Oct 2026) do not exclude Moroccan citizenship or residency; Payoneer and Airwallex gate on the entity's country; Revolut Business and UAE banks/neobanks gate on the individual's residency. Evidence for Wise Business with a Morocco-resident director is absent.

### Cited Findings
- Relay prohibits owners (incl. beneficial owners) whose citizenship or residency is: Afghanistan, Belarus, Bosnia and Herzegovina, Burkina Faso, Burma, Burundi, Cambodia, CAR, DRC, Cuba, Ethiopia, Guinea-Bissau, Haiti, Iran, Iraq, Lebanon, Libya, Mali, Nicaragua, Nigeria, North Korea, Pakistan, Russia, Somalia, South Sudan, Sudan, Syria, Ukraine, Venezuela, Yemen, Zimbabwe; otherwise US entities with non-US owners are allowed; last updated 11 Aug 2026. [O] — [Relay](https://relayfi.com/hc/en-us/articles/10239600121748-Prohibited-Countries/)
- A third-party review notes Relay's help centre also says each beneficial owner's personal address must be a physical US address, without reconciling this with accepting owners abroad. [S] — [globalsolo banking access index](https://www.globalsolo.global/data/banking-access-index)
- Mercury restricted list as reproduced by doola (published 1 Aug 2024, updated 30 Oct 2026): Afghanistan, Albania, Belarus, Bosnia & Herzegovina, Burundi, Cambodia, Cameroon, CAR, DRC, Congo, Croatia, Cuba, Eritrea, Haiti, Iran, Iraq, Lebanon, Liberia, Libya, Mali, Mozambique, Myanmar, Nicaragua, Nigeria, North Korea, Pakistan, Palestine, Philippines, Russia, Somalia, South Sudan, Sudan, Syria, Ukraine, Venezuela, Yemen, Zimbabwe; "Yes, you can apply for a US business bank account from Morocco"; needs US entity + EIN. [S] — [doola](https://www.doola.com/mercury-guide/how-to-open-a-mercury-account-in-morocco/)
- Mercury's help centre lists Morocco among countries where it cannot mail physical cards. [O-snippet] — [Mercury](https://support.mercury.com/hc/en-us/articles/34087163095572)
- Bluevine's FAQ excerpt: a non-resident with a foreign address can use Bluevine if the business is a US entity; not available to non-US entities. [O-snippet] — [Bluevine](https://www.bluevine.com/blog/introducing-bluevine-for-international-business-owners)
- Payoneer official pricing (see matrix B). Fees "depend on sender and recipient locations"; some countries have minimum withdrawal fees or registration fees. [O] — [Payoneer pricing](https://www.payoneer.com/pricing/)
- Grey (a competitor) says in one article Payoneer does not support direct MAD payouts and in another that withdrawals to Moroccan banks in MAD work; fees quoted up to 3% withdrawal and 0.5–3.5% conversion. [S, internally conflicting] — [Grey comparison](https://grey.co/blog/wise-vs-paypal-vs-payoneer-which-works-better-for-moroccans), [Grey EU clients](https://grey.co/blog/payment-options-for-moroccan-freelancers-working-with-eu-clients)
- Airwallex: business must be registered in a supported country and be active/in good standing; no stated nationality/residence restriction; sole traders accepted in some locations; passport required from every director. [O] — [Airwallex eligibility](https://help.airwallex.com/hc/en-gb/articles/900001757026-Can-I-open-an-account-with-Airwallex-)
- Airwallex documents payouts to Moroccan bank accounts. [O-snippet] — [Airwallex payout network Morocco](https://www.airwallex.com/docs/payouts/payout-network/bank-accounts/morocco)
- Wise: you can register and send from most countries, but "holding money requires living in a country where you can open a Wise account"; Bahrain, Ireland, Israel, Malaysia are personal-only for balances; Hong Kong business-only; Morocco not mentioned. [O] — [Wise countries](https://wise.com/help/articles/2978049/which-countries-can-i-use-wise-in), [Wise balances](https://wise.com/help/articles/2813542/why-cant-i-open-a-balance)
- A 2026 guide says Wise Business issues USD account details based on the business's registered address and refuses them in "dozens of countries" (examples: Nigeria, Pakistan, Türkiye, UAE). [S] — [Slash](https://www.slash.com/blog/wise-business-isnt-available)
- Wise states receiving banks in Morocco (Al Barid, Attijariwafa, BMCE, BMCI, Crédit du Maroc, SG Maroc) may charge a receiving fee up to 20 MAD on MAD transfers. [O-snippet] — [Wise MAD transfers](https://www.wise.com/help/articles/2932363/mad-transfers)
- UAE: banks generally require a UAE trade licence; non-resident shareholders can be added subject to enhanced checks; Emirates NBD, Mashreq, ADCB, FAB, HSBC, StanChart onboard some non-resident/free-zone profiles selectively; Meydan Free Zone says non-resident founders cannot activate a UAE corporate account without becoming resident. [S] — [businessdubai.ae](https://www.businessdubai.ae/blogs/uae-bank-account-non-residents), [binderr](https://binderr.com/marketplace/ae/opening-a-free-zone-company-bank-account-in-uae1)
- Estonia: official e-Residency material says the programme does not guarantee a bank account; fintech EMIs (Wise, Revolut Business, Payoneer) are the usual remote route; sources conflict on whether LHV needs an in-person visit or video KYC plus a real Estonian business link. [O]/[S] — [e-resident.gov.ee](https://www.e-resident.gov.ee/blog/posts/how-e-residents-can-avoid-common-business-account-mistakes/), [enty.io](https://enty.io/blog/stripe-wise-payoneer-or-local-bank-estonian-ou)
- Payset (an EMI not on the requested list) publishes Morocco among accepted nationalities/residencies for UBOs and directors. [O-snippet] — [Payset](https://service.payset.io/hc/en-us/articles/20393936753436-What-are-the-accepted-nationalities-and-residencies-for-UBOs-Directors-and-Authorized-Persons)

### Inferences
- For a US LLC, Relay + Mercury give two independent US accounts that do not, on paper, exclude a Morocco-resident owner; the absence of physical card delivery to Morocco at Mercury is a practical limit (virtual cards only).
- A UAE free-zone company without the founder obtaining UAE residency is likely unbankable locally, which undermines that structure unless residency is part of the plan.
- The Estonian OÜ depends on Wise/Payoneer/Revolut acceptance; since Revolut requires residence in a supported country and Wise's stance on Morocco-resident directors is unverified, the OÜ's banking is the least certain of the EU/UK options.

### Gaps
- No official Wise statement on a UK Ltd/US LLC/OÜ whose only director lives in Morocco.
- Revolut's residence-country list could not be read (403).
- No data on API access terms for Mercury, Relay, Wise, Payoneer, Airwallex (search returned only Stripe).
- Monthly fees and FX margins for Mercury, Relay, Wise, Airwallex not captured in this pass.

---

## 5. Moroccan-side rails: bank foreign-currency accounts, CMI and local PSPs

### Takeaway
A Moroccan exporter of services can receive SWIFT in USD/EUR and keep 70% of receipts in a foreign-currency account under the 2026 exchange instruction; local card acquiring (CMI and aggregators) accepts foreign Visa/Mastercard and since February 2025 offers dynamic currency conversion, but settles in MAD and no source confirms recurring-billing support.

### Cited Findings
- IGOC 2026 (in force 1 Jan 2026): exporters of goods and services may keep 70% of repatriated export receipts in a foreign-currency account with their bank, the remaining 30% being sold for dirhams; 85% for operators "categorised" by the Office des Changes per the firm's English page. [S] — [Upsilon Consulting](https://upsilon-consulting.com/export-biens-services-change-maroc/)
- Service exporters may alternatively credit the account with 15% of total contract value without invoice-by-invoice justification; not cumulable with the 70% facility. [S] — [Aujourd'hui le Maroc](https://aujourdhui.ma/?p=509824)
- IGOC 2026 e-commerce FX allowance cited as MAD 20,000/year for individuals and up to MAD 2 million/year for certified startups (outbound spending allowance). [S] — [WorldFirst](https://www.worldfirst.com/af/?p=49279)
- Receiving-side SWIFT cost estimates: 50–150 MAD per incoming transfer depending on bank (AWB, BP, CIH, BMCE) in one comparison; 100–300 MAD plus 1–3‰ exchange commission in another; negotiable. [S] — [wafir.ma](https://wafir.ma/fr/mre/transfert-argent)
- CMI + Global Blue launched e-DCC (dynamic currency conversion) for Moroccan e-commerce sites in February 2025, letting foreign cardholders pay in EUR, USD, GBP etc. [S] — [TelQuel 19/02/2025](https://telquel.ma/2025/02/19/e-commerce-le-cmi-integre-la-conversion-dynamique-des-devises-au-maroc_1918539)
- A 2026 SME guide: CMI accepts international Visa/Mastercard at roughly 2.5–3%; PayZone 1.5–2.5% per transaction; funds are paid out in dirhams to the Moroccan account; aggregators licensed by Bank Al-Maghrib (PayZone, Maroc Telecommerce, YouCan Pay) are faster to set up with slightly higher fees. [S] — [Kolonell](https://kolonell.com/fr/blog/paiement-en-ligne-pme-maroc-cmi-ou-stripe-2026)
- Bank Al-Maghrib lowered the domestic interchange cap from 0.65% to 0.50% excl. tax from 1 Oct 2026; this caps interchange only, not total merchant commission, and concerns domestic cards. [S] — [Médias24 10/07/2026](https://medias24.com/2026/07/10/paiement-par-carte-a-partir-du-1ᵉʳ-octobre-2026-bank-al-maghrib-abaisse-les-frais-dinterchange-a-050-1720115/)
- The acquiring market moved to a multi-acquirer model (CMI no longer sole acquirer), welcomed by BAM and the Competition Council. [S] — [Hespress](https://fr.hespress.com/480898-paiement-electronique-bam-et-le-conseil-de-la-concurrence-saluent-louverture-du-marche.html)
- Office des Changes audited service exporters (influencers) for non-repatriation; 72.3 bn MAD of transactions were controlled on documents in 2025. [S] — [Hespress](https://fr.hespress.com/482816-controle-sur-pieces-plus-de-723-mmdh-de-transactions-controlees-par-loffice-des-changes-en-2025.html)

### Inferences
- With MAD settlement and no confirmed subscription tooling, CMI/aggregators suit one-off sales to foreigners more than global SaaS billing; an MoR paying out by wire to a Moroccan foreign-currency account is the cleaner route for (a).
- Any balance left on PayPal/Payoneer by a Moroccan resident sits in a grey zone under exchange rules (per the Cash Plus explanation); prompt repatriation is the conservative reading.

### Gaps
- No official 2026 tariff brochures for Attijariwafa, Bank of Africa, CIH or BCP were retrieved; fees above are comparison-site estimates.
- Whether auto-entrepreneurs qualify for the 70% foreign-currency account is not addressed in any source found.
- No pricing or international-card/recurring details for YouCan Pay, NAPS, Fatourati; CMI DCC commission not published.
- The Office des Changes text on foreign wallets (PayPal/Payoneer/Wise) was not read directly.

---

## 6. App stores, marketplaces and freelance platforms

### Takeaway
Morocco is closed for selling on Google Play (no merchant registration) and for paid AWS Marketplace listings; a foreign entity in the US, UK, EU, UAE or Hong Kong fixes both. Most creator/freelance platforms reach Morocco through Payoneer or PayPal rather than direct wire.

### Cited Findings
- Google Play: Morocco supports developer registration but not merchant registration; Estonia, US, UK, UAE support both. [O] — [Google Play Console help](https://support.google.com/googleplay/android-developer/answer/9306917)
- AWS Marketplace paid products: seller must be a permanent resident/citizen of, or an entity organised in, Australia, Bahrain, Colombia, EU member states, Hong Kong, India, Israel, Japan, New Zealand, Norway, Qatar, South Korea, Switzerland, UAE, UK or US; must provide a bank account in an eligible jurisdiction able to accept USD; KYC required for EMEA sales. Morocco and Singapore are not listed. [O] — [AWS seller eligibility](https://docs.aws.amazon.com/marketplace/latest/userguide/seller-eligibility.html)
- Shopify Partners: payouts through Hyperwallet, twice monthly, minimum USD 25, 30-day hold on first-time referral earnings. [O] — [Shopify partner help](https://help.shopify.com/en/partners/getting-started/getting-paid)
- Fiverr: withdrawal options for Moroccans reported as Payoneer and bank transfer; Upwork: Payoneer widely used; Udemy pays non-US instructors via Payoneer or PayPal. [S] — [Grey](https://grey.co/blog/best-freelance-platforms-accessible-from-morocco), [Grey passive income](https://grey.co/blog/passive-income-ideas-for-moroccan-freelancers)
- Payoneer charges "varies by marketplace" for marketplace receipts. [O] — [Payoneer pricing](https://www.payoneer.com/pricing/)

### Inferences
- A Morocco-resident owner of a US/UK/EE/UAE/HK entity qualifies for AWS Marketplace through the entity, but needs a bank account located in an eligible jurisdiction, which ties back to §4.

### Gaps
- No source found for Apple App Store payouts to Moroccan banks, Microsoft Partner Center/AppSource payout countries, Chrome Web Store, Atlassian Marketplace, Apify, RapidAPI, Envato, Amazon KDP, AdSense or Malt.
- Hyperwallet's coverage of Morocco for Shopify payouts not verified.

---

## 7. Account-closure, hold and reserve risk

### Takeaway
The one well-documented, press-covered event is Mercury's July–August 2024 offboarding of customers tied to a list of restricted countries; Morocco was not reported as affected. Reports of Stripe reserves and Payoneer/Wise freezes are anecdotal or from firms selling compliance services.

### Cited Findings
- Mercury told affected customers in July 2024 their accounts would close on 22 Aug 2024; scope was founders living in or businesses headquartered/with addresses in restricted countries (Nigeria, Ukraine, Pakistan, Croatia and others); Mercury said passports were not considered; trigger linked to regulatory scrutiny of partner Choice Bank; affected customers held under 1% of deposits. [S, reputable press] — [TechCrunch 23/07/2024](https://techcrunch.com/2024/07/23/mercury-bank-fintech-sanctions-ukraine-nigeria), [TechCabal](https://techcabal.com/2024/07/23/us-bank-mercury-to-close-accounts-of-nigerian-startups/)
- Relay notes its prohibited list derives from Thread Bank policy, US sanctions and federal law; a reviewer notes such partner-bank lists can change without notice. [O]/[S] — [Relay](https://relayfi.com/hc/en-us/articles/10239600121748-Prohibited-Countries/), [globalsolo](https://www.globalsolo.global/data/banking-access-index)
- Stripe Managed Payments requires a "low historical dispute rate and no prior risk issues" for continued eligibility. [O] — [Stripe eligibility](https://docs.stripe.com/payments/managed-payments/eligibility)
- Forum reports: Stripe account "under review" with ~USD 14k frozen (June 2026), later released; a 25% rolling reserve imposed without warning (late 2025); an Atlas founder with ~USD 8,200 frozen after an enhanced due-diligence request. [A] — [terms.law forum](https://terms.law/forum/thread/stripe-account-review-frozen-june-2026.html), [terms.law megathread](https://www.terms.law/forum/thread/megathread-payment-processor-disputes-2026.html)
- A consultant blog claims about 90% of non-resident Stripe closures stem from mismatches between information given to Stripe and IRS/state records. [A, unverified single source] — [ustaxreport blog](https://ustaxreport-hpqohmax.manus.space/blog/stripe-closes-nonresident-accounts)
- Review aggregation: recurring Payoneer complaints about accounts frozen/closed with little warning and funds locked for weeks or months (23 explicit mentions on G2). [A] — [checkthat.ai](https://checkthat.ai/brands/payoneer/reviews)
- Dodo keeps grandfathered merchants "under enhanced monitoring". [O] — [Dodo docs](https://docs.dodopayments.com/miscellaneous/accepted-countries-and-territories)

### Inferences
- Legitimate risk reducers supported by the sources: identical legal name/EIN/address data across IRS, state registry, bank and processor; truthful residence declarations; a business model matching what was declared at onboarding; low dispute and refund rates; not concentrating all funds in one fintech whose partner bank can change its country list.
- Because partner-bank lists have changed abruptly before (Mercury 2024, Dodo March 2026), a second independent account and a rapid sweep to a Moroccan bank limit exposure.

### Gaps
- No evidence found of a 2025 Mercury offboarding wave; only the 2024 event is documented.
- No regulator or CFPB-level data on freezes specific to non-resident-owned LLCs.
- No documented Wise freeze cases from 2025–2026 found.

---

## 8. Crypto / stablecoin payouts: legal status in Morocco

### Takeaway
As of late October 2026 Morocco still has no adopted crypto-asset law; draft law n° 42.25 is listed among 2027 priorities, so stablecoin payouts should be excluded or flagged for a Moroccan resident.

### Cited Findings
- Hespress, 27 Oct 2026: the government plans to adopt a dedicated legal framework through draft law n° 42.25, first version prepared end of October 2025; it appears in the PLF 2027 presentation note among priorities for 2027. [S] — [Hespress](https://fr.hespress.com/494036-plf-2027-le-gouvernement-passe-a-lencadrement-des-cryptomonnaies.html)
- The preliminary draft (dated 5 Aug 2025, published Nov 2025) was prepared by the Finance Ministry with Bank Al-Maghrib and the AMMC; it provides a licensing regime for service providers, AML rules and the Travel Rule. [S] — [Médias24 03/11/2025](https://medias24.com/2025/11/03/crypto-actifs-le-maroc-devoile-un-avant-projet-de-loi-pour-encadrer-le-secteur/)
- BAM governor Jouahri said in November 2024 the bill was "in the adoption circuit"; a draft had existed since end 2022. [S] — [Médias24 27/11/2024](https://medias24.com/2024/11/27/abdellatif-jouahri-un-projet-de-loi-encadrant-les-cryptoactifs-est-dans-le-circuit-dadoption/)
- Stripe (stablecoin payouts, public preview) and Whop (crypto wallet payouts) offer crypto payout options. [O]/[O-snippet] — [Stripe](https://docs.stripe.com/global-payouts/recipient-requirements), [Whop](https://docs.whop.com/manage-your-business/manage-payouts/payout-methods)

### Inferences
- Until 42.25 is enacted and licensed providers exist, the 2017 prohibition position remains the operative baseline; crypto payout options offered by platforms are not a compliant route for a Moroccan resident.

### Gaps
- The exact text and scope of the 2017 Office des Changes / BAM communiqué was not retrieved in this pass.
- Whether Morocco is on Stripe's stablecoin recipient-country list was not checked.

---

## 9. API / automation friendliness

### Takeaway
Only Stripe was verified: it has scoped restricted keys, agent-tagged keys and agent tooling. No terms or API documentation were read for the banks, EMIs or other MoRs.

### Cited Findings
- Stripe restricted API keys can be scoped per resource/action, IP-allowlisted, given expiry and scheduled rotation; a key can be tagged as an agent key. [O-snippet] — [Stripe keys](https://docs.stripe.com/keys/customize-api-key-permissions)
- Stripe docs advertise agent skills/plugins and `stripe agent setup`. [O] — [Stripe docs](https://docs.stripe.com/connect/cross-border-payouts)
- Stripe publishes Developer Terms for "Stripe Projects (Preview)" that define an "Agent" and make the account holder responsible for ending an agent's authority. [O-snippet] — [Stripe legal](https://stripe.com/legal/projects-developer-terms)
- A third-party tracker reports a Stripe terms clause prohibiting "pass-through agent use". [S, unverified] — [conductatlas](https://conductatlas.com/platform/stripe/stripe-terms-of-service/prohibition-on-pass-through-agent-use/)
- Global Payouts are API-driven (Outbound Payments, Outbound Setup Intents, Accounts v2). [O] — [Stripe changelog](https://docs.stripe.com/changelog/clover/2025-12-15/cross-border-payouts-new-countries)

### Inferences
- Stripe is the most agent-ready option on the evidence gathered, but it is only reachable through structure (b).

### Gaps
- No verification of API availability or agent/automation clauses for Mercury, Relay, Wise, Payoneer, Airwallex, Paddle, Lemon Squeezy, Creem, Polar, CMI or Moroccan banks.
