# Micro-SaaS, vertical SaaS, paid APIs, data products and vertical agents — opportunities for an agent-operated solo owner in Morocco (state as of 11 Nov 2026)

Reading conventions used throughout:
- **[V]** = read by me on the primary/official page on 2026-11-11. **[S]** = taken from a search-result summary of the cited page (page itself not opened, or it blocked fetching) — treat as "to re-verify". **[SR]** = founder self-reported revenue, not payment-verified. **[EST]** = my own estimate/judgment, not a sourced fact.
- All access dates are 2026-11-11 unless a publication date is given.
- Several aggregator pages (BigIdeasDB, Saas Hero, Fungies, Dodo Payments) are vendors with a commercial interest; BigIdeasDB returned HTTP 429 and Indie Hackers HTTP 403 on direct fetch, so their numbers are [S] only.

---

## Q0. Inventory of 25 distinct product-type opportunities

### Takeaway
Demand evidence exists for almost every product type, but it is dominated by outliers: every category has one or two five-figure-MRR solo examples and a documented long tail earning roughly zero. The types with the best combination for this owner (payable from Morocco, built-in distribution, not replaceable by a chat window, low capital) are marketplace apps with 0% platform fee (Shopify, Atlassian Forge), continuously refreshed data/alert products (tenders, pharma, jobs, company, prices) and Apify/API listings; low-ticket AI wrappers and Android paid apps are the weakest.

### Cited Findings

Build difficulty, automatable share and capital are **[EST]** in every row (no source measures them); everything else is sourced or marked as a gap.

**A. Marketplace apps (built-in distribution)**

1. **Shopify App Store utility app** (niche merchant workflow). Who pays: merchants, monthly. Proof: a solo founder reports ~$1.03M ARR at start of 2026 and ~$125k MRR by June 2026 [SR][S] — [Indie Hackers](https://www.indiehackers.com/post/hitting-125k-mrr-as-a-solo-founder-by-doubling-down-on-the-right-segment-c4o2Tfs6mjdpip5yZhaO); a freelancer-built portfolio at "$100k+ MRR" [SR][S] — [Indie Hackers](https://www.indiehackers.com/post/qdReVAgLjz6EpW4OrJSI). Counter-evidence: a May 2026 index counted 21,509 live public apps, 2,713 launched in that single month; third-party estimates put the median listed app under $1,000/month and say the 16 largest apps take 40% of revenue [S; exact page attribution among the following not verified] — [BigIdeasDB](https://bigideasdb.com/shopify-app-vs-wordpress-plugin), [AdsX](https://adsx.com/blog/how-much-shopify-app-developers-make), [Barn2](https://barn2.com/?p=712947). Fee: 0% on first $1,000,000 lifetime gross app revenue, 15% above; revenue before 1 Jan 2025 not counted [S, official doc] — [Shopify.dev](https://shopify.dev/docs/apps/launch/distribution/revenue-share). Build [EST]: medium (OAuth, billing API, app review). Automatable [EST]: ~70-80%; support and review responses are the human residue. Capital [EST]: <$300. Failure: buried in search ("page 29", 0 installs in 7 days anecdotes [S]), 2,700 launches/month. Defensibility: reviews and rank accumulate; data stays in merchant store.
2. **Atlassian Marketplace Forge app** (Jira/Confluence add-on). Fee: 0% on Forge revenue until $1M lifetime Forge revenue (Atlassian calls the incentive temporary); standard Forge share moves 15%→16%→17% during 2026 (two Atlassian posts give different effective dates: 1 Jan/1 Jul vs 1 Apr/1 Oct 2026) [S, official] — [Atlassian blog](https://www.atlassian.com/blog/developer/updates-to-marketplace-revenue-share-2026), [Atlassian extended timelines](https://www.atlassian.com/blog/developer/extended-timelines-for-marketplace-revenue-share-changes), [Runs on Atlassian 100%](https://www.atlassian.com/blog/developers/runs-on-atlassian-apps-can-now-take-home-100-of-marketplace-revenue). Who pays: B2B teams per user, monthly/annual. Build [EST]: medium-high (Forge platform constraints, security review). Defensibility: enterprise procurement prefers marketplace billing; fewer vibe-coded entrants than consumer stores.
3. **Chrome extension (freemium or one-time)**. Proof: Superpower ChatGPT, solo developer, ~$20-30k MRR [SR, via podcast summary] — [StationLM summary of Starter Story](https://stationlm.com/analysis/f49eff9c-de2f-4f9a-9f49-f32db058cc58); a $29 one-time extension with >$20k since January 2026 and ~822 sales plus a $6.99/month upsell [SR] — [Reddit snapshot, Jun 2026](https://reddit.sentinel-team.org/posts/1u35tpj/snapshots/2026-06-12T13%3A50%3A43.301242Z). Counter-evidence: a developer with 38 live extensions reports ~$31 MRR and ~$165 lifetime net revenue (Jul 2026) [SR] — [DEV Community](https://dev.to/_350df62777eb55e1/real-numbers-freemium-chrome-extension-monetization-after-6-months-5hga); another reports $22/month (May 2026) [SR] — [Indie Hackers](https://www.indiehackers.com/post/mrr-update-22-month-from-chrome-extensions-05b6ca4f40). Cost: one-time $5 developer registration [S] — [9to5Google](https://9to5google.com/2020/03/12/chrome-web-store-fee/). Payment is collected outside the store (e.g. ExtensionPay reported at 5% + Stripe fees, from a competitor's guide, unverified) — [Fungies](https://fungies.io/monetize-chrome-extension-2026.md). Build [EST]: low. Failure: platform policy/Manifest changes, host site ships the feature, payment-flow drop-off.
4. **WordPress plugin (freemium on WordPress.org, paid via Freemius)**. Proof: in a 40-product verified WordPress sample (Sep 2026), 10.0% clear $1,000/month; top five range $997-$8,108/month [S; tiny sample] — [BigIdeasDB](https://bigideasdb.com/how-to-sell-a-wordpress-plugin); Freemius case: "$5,000 MRR in 5 months" (vendor marketing) [S] — [Freemius customers](https://freemius.com/wordpress/customers/). Fees: Freemius lowered rates on 1 Oct 2025; a Nov 2025 founder interview lists 4.7% base + 2.3% WordPress add-on, i.e. 7% after $5,000 lifetime sales [S; verify on pricing page] — [Latka interview](https://getlatka.com/companies/freemius.com/interviews/freemius-vova-feldman-2025). Freemius lists Morocco among supported countries [S] — [Freemius docs](https://freemius.com/help/documentation/selling-with-freemius/supported-countries). Recurring: annual licences. Build [EST]: low-medium.
5. **iOS app / subscription utility**. Fee: 15% under Apple's Small Business Program (<$1M proceeds prior year) [S] — [Apple newsroom](https://www.apple.com/in/newsroom/2020/11/apple-announces-app-store-small-business-program/). Morocco eligibility for Apple payouts not confirmed by any source found (gap).
6. **Android paid app / in-app purchases — NOT available directly**. Google's official table shows Morocco: developer registration ✔, merchant registration ✘ ("Location does not support merchants"); Algeria, Tunisia and Egypt are ✔ for merchants [V] — [Google Play Console Help](https://support.google.com/googleplay/android-developer/answer/9306917). A Morocco-resident individual cannot sell paid apps/IAP on Google Play without a foreign entity; ads-only or web-billed models remain.
7. **HubSpot / Slack / AWS Marketplace apps**. No current fee or solo-revenue data retrieved; the only HubSpot figure found (20% of net revenue) is the Solutions Partner referral commission, not an app-store fee [S] — [HubSpot partner policies](https://www.hubspot.com/partners/sales/program-policies). Treat as unverified (gap).

**B. APIs and scraping/automation listings**

8. **Apify Store actors (scrapers/automations sold per event)**. Terms: creators keep 80% of pay-per-event revenue, minus platform usage costs; rental model stopped accepting new listings 1 Apr 2026 and was retired 1 Oct 2026 [S, official docs] — [Apify docs](https://docs.apify.com/actors/monetize.md), [pay-per-event](https://docs.apify.com/actors/publishing/monetize/pay-per-event.md). Scale: 25,787 actors, 3,015 active publishers (May 2026); pay-per-event = 66% of catalog and 87% of demand [S] — [SignalCensus](https://signalcensus.pages.dev/articles/apify-store-may-2026-25787-actors-480k-mau). Apify marketing claims creators were paid >$1M "last month", many >$3k (company claim) [S] — [UsagePricing/Apify](https://usagepricing.com/blueprint/apify). Counter-evidence: a developer reported $0 revenue despite 5,407 results because users were on the free plan; another launched 13 Korean scrapers (2,000 runs in 3 days; final revenue not retrieved) [SR] — [DEV Community](https://dev.to/sessionzero_ai/2000-runs-in-3-days-real-revenue-data-from-launching-13-korean-scrapers-on-apify-211h). Build [EST]: low; maintenance = sites change, well suited to agents. Legal: only public data and ToS-compliant targets.
9. **Paid API on RapidAPI**. Fee: flat 25% marketplace fee (20% in older docs; increase effective 15 Nov 2025 per a secondary source); payouts via PayPal only, PayPal fee extra [S, official docs] — [RapidAPI docs](https://docs.rapidapi.com/docs/payouts-and-finance). A third-party reading of the ToS says fees can change with 7 days' notice [S] — [ConductAtlas](https://conductatlas.com/platform/rapidapi/rapidapi-terms-of-use/7-day-transaction-fee-modification-notice/). PayPal lists Morocco as "send, receive, and withdraw" [S] — [PayPal developer docs](https://developer.paypal.com/payouts/supported-features).
10. **Agent-ready data endpoints (MCP servers over a niche dataset)**. Evidence that incumbents now ship MCP access: Apify actors expose `/api/mcp` endpoints for tender data — [Apify actor](https://apify.com/datapilot/public-tender-procurement-alerts/api/mcp); job-data vendors publish "jobs MCP" comparisons — [TheirStack](https://theirstack.com/en/blog/best-jobs-mcp). No revenue data found for MCP-only products (gap).

**C. Value-added data products (public prices found)**

11. **Tender / public-procurement alerts and API** (Morocco, francophone Africa, or a sector slice). Prices: OpenOpps Solo £120 per user/month [S] — [OpenOpps pricing](https://www.openopps.com/pricing); Tenders-SA developer API R299/month for 50,000 requests, subscriptions R499 and R1,299/month (the two pages conflict) [S] — [Tenders-SA developers](https://www.tenders-sa.org/developers), [tiers](https://www.tenders-sa.org/documentation/user-guides/subscription-tiers); Australian Tenders plan at $145/month [S] — [Australian Tenders](https://www.australiantenders.com.au/pricing/); Tenders Agent (India) ₹2,999-₹9,999/year [S] — [Capterra](https://www.capterra.com/p/10056461/Tenders-Agent/pricing/); Tendios keeps API on top tier only [S] — [Tendios](https://tendios.com/en/bidders/pricing). Low-end commoditisation: Apify tender actors at $10/month + usage and "from $0.10 per 1,000 results" for SAM.gov + TED [S] — [Apify actor 1](https://apify.com/datapilot/public-tender-procurement-alerts/api/mcp), [Apify actor 2](https://apify.com/taroyamada/procurement-intel-actor/api/mcp). Who pays: SMEs bidding on contracts. Recurring: high (daily freshness). Defensibility: local-language coverage, document parsing, matching quality.
12. **Pharma data: drug registry / price / shortage tracking**. Prices: pharmazie.com (Germany) lists modules at ~€50-€250 per user/month billed annually, an API plan (up to 5,000 entries) at €250 per user/month, and supply-shortage tracking as a €50 per user/month add-on [S] — [pharmazie.com pricing](https://go.pharmazie.com/pricing). Larger incumbents are quote-only: Medi-Span Price Rx — [Wolters Kluwer](https://wolterskluwer.com/en/solutions/medi-span/about/pricing-policy-update); Micromedex RED BOOK — [Merative](https://www.merative.com/clinical-decision-support/micromedex-redbook); GlobalData POLI (prices in 80 markets) — [GlobalData](https://hot-topics.globaldata.com/marketplace/pharmaceuticals/pharmaceutical-prices-poli-database/); Global Pricing Innovations — [Datarade](https://datarade.ai/data-providers/global-pricing-innovations-limited/profile). No solo-founder revenue data found for this niche; no Morocco/Maghreb-specific paid product found in this research (gap, not proof of absence).
13. **Job-postings data API / hiring-signal feed**. Prices (conflicting secondary sources): TheirStack $49/month with free tier vs $59/month [S] — [OpenWeb Ninja](https://www.openwebninja.com/blog/best-job-data-apis-2026), [Prospeo](https://prospeo.io/s/theirstack-pricing-reviews-pros-and-cons); Coresignal $49/month (Mini) to $5,000/month (Elite) per one source, "from $250/month" per Coresignal's own blog [S] — [JobsPipe](https://jobspipe.dev/blog/coresignal-pricing), [Coresignal](https://coresignal.com/blog/best-job-posting-data-providers-comparison-and-use-cases/); JobsPikr quote-only. Crowded global market; a regional slice (MENA/Africa/French) is the only plausible solo angle [EST].
14. **Company / registry data API**. Prices: OpenCorporates Essentials £2,250/year (500 calls/month), Starter £6,600/year, Basic £12,000/year, Enterprise custom [S, official page] — [OpenCorporates pricing](https://opencorporates.com/pricing/). Pappers (France): credit-based monthly packs, 100 free credits, 1 credit per company profile; amounts not retrieved [S] — [Pappers API](https://www.pappers.fr/api).
15. **Competitor price monitoring (SaaS + data)**. Prices (third-party, conflicting): Prisync $59-$100/month entry to a $399 Platinum plan with API at +20%; Price2Spy entry quoted at $19.95, $39.95 (500 URLs, checked 2026-10-12) or $67.95 (2026-05-06) [S] — [Capterra Prisync](https://www.capterra.com/p/153451/Prisync/pricing/), [Pulse Signal](https://getpulsesignal.com/pricing/prisync), [xpay](https://www.xpay.sh/saas-pricing/price2spy/). Who pays: e-commerce merchants. Angle [EST]: a single vertical or country's retailers.
16. **Regulatory/compliance monitoring for a narrow vertical**. An Indie Hackers post contrasts saturated "AI writing assistant" with unsaturated "automated compliance evidence for Kubernetes infra teams" (opinion) [S] — [Indie Hackers](https://www.indiehackers.com/post/vibe-coding-is-quietly-killing-simple-saas-products-the-thing-thats-actually-defensible-isn-t-a-feature-it-s-the-boring-layer-3a785dadf1). No prices or MRR retrieved (gap).

**D. Directories, templates, digital products, content**

17. **Curated paid directory**. OpenAlternative reported >$6,500/month [SR] — [IndieNiche](https://indieniche.substack.com/p/how-he-turned-his-open-source-directory); a directory portfolio at $13k/month [SR] — [Indie Hackers](https://www.indiehackers.com/post/doubling-down-on-directories-to-hit-13k-mo-2KasH9NLK3ehlTL9GeGO). Revenue is mostly sponsorship/listing fees, SEO-dependent.
18. **Boilerplate / starter kit (one-time sale)**. Dirstarter ~$5k/month (headline elsewhere says "$30K business") [SR] — [Indie Hackers](https://www.indiehackers.com/post/how-i-turned-my-copycats-into-customers-from-open-source-directory-to-5k-month-boilerplate-ce615af4f6); Marc Lou (ShipFast and others) self-reported ~$81.7k income for Feb 2026, not split by product [SR] — [IndieAI](https://indieai.pages.dev/blog/marc-lou-81683-february-2026-income-breakdown). Audience-dependent; non-recurring.
19. **Notion / template libraries**. Easlo "0 to $20k/mo" [SR] — [Indie Hackers stories](https://www.indiehackers.com/stories); a Notion tool listed for sale at "$3k MRR, 80% margins, 6 hrs/week" (listing claim) — [ShipByData](https://shipbydata.pages.dev/en/startup/notion-tool-with-3k-mrr-80-margins-6-hrs-week-ops). Driven by a 356k-follower audience in Easlo's case, not by the product.
20. **Software review / comparison site (affiliate + sponsorship)**. "5-figure-MRR software review site" [SR] — [Indie Hackers](https://www.indiehackers.com/post/building-a-5-figure-mrr-software-review-site-akoLUha2xmqFMEzSXd7z). Headwind: Flippa sold content deals fell 39% half-on-half in H1 2026 and pure SEO content is discounted without owned audience [V] — [Flippa H1 2026](https://flippa.com/blog/digital-ma-insights-h1-2026/), [Flippa Q2 2026](https://flippa.com/blog/digital-ma-market-trends-2026-q2/).
21. **Newsletter as a data product**. A 92,000-subscriber AI newsletter (38% open rate, ~$300 sponsorship revenue) sold for $20,500 in 22 days [V] — [Microns newsletter](https://newsletter.microns.io/p/2025-year-in-review).

**E. Vertical SaaS and agents**

22. **High-ticket vertical AI agent (>$250/month, B2B workflow)**. Retention evidence: AI-native products priced >$250/month show median GRR 70% / NRR 85%, "essentially the same" as B2B SaaS [V] — [ChartMogul, Dec 2025](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/). Flippa's new "AI Apps & Tools" category: 14 sales, $535,714 average price in H1 2026 [V] — [Flippa](https://flippa.com/blog/digital-ma-insights-h1-2026/). Build [EST]: high (integration, reliability, sales conversations — least automatable).
23. **Low-ticket AI wrapper (<$50/month) — anti-opportunity**. Median GRR 23% / NRR 32% for AI-native products under $50/month, ~20 points worse than B2B or B2C SaaS; users "treat them as trials" [V] — [ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/).
24. **Mid-ticket vertical micro-SaaS ($50-$249/month)**. AI-native GRR 45% / NRR 61% in this band; annual plans add 10-20 points of NRR [V] — [ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/). LinkedIn-outreach tool listed at $21,400 annual revenue for $77,000 [V] — [Microns](https://newsletter.microns.io/p/2025-year-in-review).
25. **Buy-and-improve micro-asset** (plugin, Shopify app, extension). Listings seen: Shopify security app $1,900 ARR asking $5,500; WordPress webinar plugin $10,000 revenue asking $32,000 [V] — [Microns](https://newsletter.microns.io/p/2025-year-in-review). See Q3.

### Inferences
- The same shape repeats across types: one visible outlier and a measured long tail near zero. Product type matters less than (a) whether the product depends on continuously refreshed or proprietary data, and (b) whether a marketplace sends buyers.
- Data/alert products (11-15) have the clearest public price points ($10 to ~£1,000 per month) and a job description — monitor sources, normalise, alert — that maps directly onto what agents do unattended.
- Types 17-21 depend on audience or search traffic, both of which are declining assets in 2026 per Flippa's data.

### Gaps
- No founder-published MRR found for tender, pharma, company-data or price-monitoring products run by solo founders; proof of demand there rests on incumbents' public prices only.
- Per-type churn benchmarks do not exist in the sources found; only price-band retention (ChartMogul) is available.
- Slack, HubSpot, AWS Marketplace, Microsoft AppSource fees and Chrome Web Store current policies were not confirmed from official pages.
- Most comparable prices are [S]; each should be re-opened on the vendor page before being quoted in a final report.

---

## Q1. Verified solo-founder revenue, MRR distributions and failure rates

### Takeaway
On payment-verified data the typical revenue-reporting startup earns on the order of $140/month and well under half of tracked startups report any revenue; five-figure MRR is roughly the top 1-2%. Published "success stories" are a survivor sample.

### Cited Findings
- Of 8,699 startups tracked on TrustMRR (Stripe/Paddle/Polar API-key verified), 3,787 report revenue; median MRR among those is $145 (Jul 2026); an earlier cut gave ~$136 across 3,478; only 1.2% of tracked startups exceed $50,000 MRR [S] — [BigIdeasDB State of Indie SaaS Revenue 2026](https://bigideasdb.com/state-of-indie-saas-revenue-2026), [Micro SaaS Trends 2026](https://bigideasdb.com/micro-saas-trends-2026).
- Mean MRR is cited at $4,682 — about 30x the median; one category shows a $125 median with a $22,515 average because of a single >$3.5M MRR outlier [S] — [BigIdeasDB benchmarks](https://bigideasdb.com/trustmrr-saas-revenue-benchmarks-2026).
- The same vendor's pages disagree with each other: "median SaaS ~ $7 MRR", "AI category median $203", "$2,100 median for bootstrapped SaaS" [S] — [BigIdeasDB by category](https://bigideasdb.com/saas-revenue-benchmarks-by-category-2026), [revenue benchmarks docs](https://bigideasdb.com/docs/revenue-benchmarks).
- An independent analysis of 5,079 Stripe-verified startups exists but could not be read (HTTP 403) — [Indie Hackers](https://www.indiehackers.com/post/i-analyzed-5-079-stripe-verified-startups-f0f6bd053f).
- Unverified secondary claims: 70% of micro-SaaS products earn under $1,000/month; 75% of new tools see a sharp traffic decline within a month of launch [S; original source not identified] — [abhs.in](https://abhs.in/blog/vibe-coding-saas-flood-pmf-failure-user-acquisition-reality-2026), [LavX](https://news.lavx.hu/article/the-sideprocalypse-why-indie-saas-dreams-are-dying-in-2026).
- Portfolio reality check: 38 Chrome extensions → ~$31 MRR after six months [SR] — [DEV Community](https://dev.to/_350df62777eb55e1/real-numbers-freemium-chrome-extension-monetization-after-6-months-5hga).

### Inferences
- TrustMRR itself is biased upward (founders opt in to show revenue), so $145 median is an optimistic bound for "a launched product", and 3,787/8,699 ≈ 44% reporting any revenue is likewise optimistic.
- A realistic planning base case for one launched product is $0-$200 MRR after six months; plans should assume a portfolio of attempts and a small probability of a $1k+ MRR product.

### Gaps
- No official TrustMRR statistics page; all distribution figures come from one third-party vendor with internal inconsistencies.
- No reliable failure-rate (shutdown) statistic by category; Starter Story and Acquire.com official data not retrieved.

---

## Q2. Marketplaces: fees and whether a Morocco-based developer can get paid

### Takeaway
The decisive constraint is payment rails, not fees: Google Play does not support merchants in Morocco and Stripe does not open Moroccan accounts, while merchant-of-record platforms (Lemon Squeezy, Paddle, Polar, Freemius) and PayPal list Morocco. Shopify and Atlassian currently charge 0% on the first $1M, but their Morocco payout support was not confirmed.

### Cited Findings
- Google Play: Morocco developer registration ✔, merchant registration ✘ [V] — [Google Play Console Help](https://support.google.com/googleplay/android-developer/answer/9306917).
- Stripe: no standard merchant accounts in Morocco (multiple vendor blogs; a Sept 2026 WorldFirst page says "not currently supported"); Stripe's Dec 2025 changelog adds `ma_bank_account` as a cross-border payout recipient country, i.e. platforms using Stripe can pay out to Moroccan banks [S] — [WorldFirst](https://www.worldfirst.com/af/blog/business-banking-insights/stripe-review-africa/), [Stripe changelog](https://docs.stripe.com/changelog/clover/2025-12-15/cross-border-payouts-new-countries).
- Lemon Squeezy: Morocco is in the list of countries with bank payouts; PayPal payouts in 200+ countries [V] — [Lemon Squeezy docs](https://docs.lemonsqueezy.com/help/getting-started/supported-countries). Payouts twice monthly after a 13-day hold [S] — [Lemon Squeezy getting paid](https://docs.lemonsqueezy.com/help/getting-started/getting-paid).
- Paddle: Morocco (MA) appears in the supported-countries table, but that page covers where Paddle sells; seller/payout eligibility for Morocco was not confirmed [S] — [Paddle developer docs](https://developer.paddle.com/concepts/sell/supported-countries-locales), [Paddle help](https://www.paddle.com/help/start/account-verification/which-countries-are-supported-by-paddle). Paddle pays monthly with a $100 minimum [S] — [GlobalSolo comparison](https://www.globalsolo.global/compare/services/paddle-vs-lemon-squeezy).
- Polar and Freemius each publish supported-country lists reported to include Morocco [S] — [Polar docs](https://polar.sh/docs/merchant-of-record/supported-countries.md), [Freemius docs](https://freemius.com/help/documentation/selling-with-freemius/supported-countries).
- PayPal: Morocco is "send, receive, and withdraw" [S] — [PayPal developer docs](https://developer.paypal.com/payouts/supported-features).
- Shopify: 0% on first $1M lifetime, 15% above, computed on gross [S] — [Shopify.dev](https://shopify.dev/docs/apps/launch/distribution/revenue-share). Partner payouts are by PayPal or local/wire transfer "depending on region"; no document naming Morocco was found [S] — [Shopify partners blog](https://www.shopify.com/my/partners/blog/payout-methods).
- Atlassian: 0% until $1M lifetime Forge revenue (temporary), otherwise 16-17% in 2026 [S] — [Atlassian](https://www.atlassian.com/blog/developer/updates-to-marketplace-revenue-share-2026).
- Apple: 15% under the Small Business Program [S] — [Apple](https://www.apple.com/in/newsroom/2020/11/apple-announces-app-store-small-business-program/).
- RapidAPI: 25%, PayPal-only payouts [S] — [RapidAPI docs](https://docs.rapidapi.com/docs/payouts-and-finance). Apify: creator keeps 80% of pay-per-event minus compute [S] — [Apify docs](https://docs.apify.com/actors/monetize.md).
- Chrome Web Store: $5 one-time registration [S] — [9to5Google](https://9to5google.com/2020/03/12/chrome-web-store-fee/). Freemius ~7% [S] — [Latka](https://getlatka.com/companies/freemius.com/interviews/freemius-vova-feldman-2025).
- Moroccan developers have publicly asked Google to enable app monetisation (undated article) [S] — [Bladi](https://en.bladi.net/moroccan-tech-experts-urge-google-enable-app-monetization-morocco,86947.html).

### Inferences
- A merchant-of-record with confirmed Morocco bank payouts (Lemon Squeezy confirmed; Paddle/Polar/Freemius to confirm) is the default billing stack; it also removes VAT/sales-tax handling from the owner.
- Marketplaces that bill on the developer's behalf and pay via PayPal (RapidAPI, probably Shopify) are reachable through PayPal Morocco; Android paid distribution is not, short of a foreign entity.

### Gaps
- Official confirmation of Morocco for Shopify Partner payouts, Atlassian vendor payouts, Apple developer payouts and Apify payouts was not found.
- Moroccan foreign-exchange and tax treatment of service-export receipts (Office des Changes, auto-entrepreneur ceilings) is outside this research and must be checked.
- Whether Lemon Squeezy still onboards new stores following its acquisition by Stripe was not addressed on the page read.

---

## Q3. Acquisition multiples — is buying with 15,000-60,000 MAD (~$1,500-6,000) realistic?

### Takeaway
Not for a genuinely profitable SaaS: the median Acquire.com ask is ~$190k and profit multiples are ~2.5-4x, so $1,500-6,000 buys an asset earning roughly $40-200/month in profit, or a pre-revenue project. Such listings exist (e.g. a Shopify app at $1,900 ARR for $5,500) but they are closer to buying code plus a listing than buying a business.

### Cited Findings
- Acquire.com listings (third-party analysis, Jun 2026): median asking price $190k across 615 listings ($195,800 across 651; middle 50% $75,000-$512,550); median ~2.0x TTM revenue and 3.4x TTM profit; SaaS 3.60x profit / 2.30x revenue; AI listings 5.10x profit; closed deals at median 3.9x profit in 2024 and 2025 [S] — [BigIdeasDB valuations](https://bigideasdb.com/state-of-saas-valuations-2026), [BigIdeasDB acquisitions](https://bigideasdb.com/state-of-saas-acquisitions-2026).
- Flippa H1 2026 average profit multiples on sold deals: SaaS 2.47x (top quartile 4.06x), apps 2.62x, content sites 2.32x, ecommerce 1.55x; by size, $10K-$100K deals average 2.24x [V] — [Flippa](https://flippa.com/blog/digital-ma-insights-h1-2026/). Flippa reports nothing for deals under $10K.
- Flippa demand: 123,022 active buyers in H1 2026 (+18% year on year); SaaS sold deals +21%, content -39% half-on-half [V] — [Flippa](https://flippa.com/blog/digital-ma-insights-h1-2026/).
- Flippa fees (third-party review): $29 listing for assets under $10K; 10% success fee under $50K [S] — [Hackceleration](https://www.hackceleration.com/labs/flippa-pricing).
- Microns listings: $5,500 for $1,900 ARR (~2.9x revenue); $32,000 for $10,000 revenue; $77,000 for $21,400 revenue; a 92k-subscriber newsletter sold for $20,500 [V] — [Microns](https://newsletter.microns.io/p/2025-year-in-review).
- Tiny Acquisitions positions itself as a marketplace for internet businesses priced under $5,000 [S] — [Product Hunt](https://www.producthunt.com/products/tiny-acquisitions).

### Inferences
- At ~3x revenue asks seen on Microns, $6,000 buys about $2,000 of annual revenue (~$165/month); at 2.2-3.9x profit, $6,000 buys ~$1,500-2,700 annual profit. Payback is 2-4 years before any improvement, with high risk that revenue is decaying.
- The defensible use of this budget is acquiring distribution cheaply (an existing listing with reviews, installs or an email list) that agents can then rebuild and improve — not acquiring cash flow.
- Abundant buyers (123k active on Flippa) versus thin sub-$10k quality supply implies adverse selection at the bottom of the market.

### Gaps
- No sold-price distribution for deals under $10k on any marketplace; Empire Flippers data not retrieved; Acquire.com's own report not found.
- Whether a Moroccan buyer can use the marketplaces' escrow and pay in foreign currency within exchange-control allowances was not researched.

---

## Q4. Paid data products and APIs — niches with paying customers and public prices

### Takeaway
Public prices confirm paying customers in tenders (~$10 to £120+/user/month), pharma data (€50-250/user/month), jobs data ($49 to $5,000/month), company data (£2,250-£12,000/year) and price monitoring (~$20-$399/month). The low end is being commoditised by per-result scrapers at cents per thousand records.

### Cited Findings
- Tenders: OpenOpps £120/user/month; Tenders-SA R299-R1,299/month; Australian Tenders $145/month; Tenders Agent ₹2,999-₹9,999/year; Apify actors $10/month or $0.10 per 1,000 results [S] — [OpenOpps](https://www.openopps.com/pricing), [Tenders-SA](https://www.tenders-sa.org/developers), [Australian Tenders](https://www.australiantenders.com.au/pricing/), [Capterra](https://www.capterra.com/p/10056461/Tenders-Agent/pricing/), [Apify](https://apify.com/taroyamada/procurement-intel-actor/api/mcp).
- Pharma: pharmazie.com €50-€250/user/month, API €250, shortage add-on €50; Medi-Span, RED BOOK, GlobalData POLI, GPI are quote-only [S] — [pharmazie.com](https://go.pharmazie.com/pricing), [Datarade GPI](https://datarade.ai/data-providers/global-pricing-innovations-limited/profile).
- Jobs: TheirStack $49-59/month; Coresignal $49 or $250 to $5,000/month; JobsPikr quote-only [S] — [OpenWeb Ninja](https://www.openwebninja.com/blog/best-job-data-apis-2026), [JobsPipe](https://jobspipe.dev/blog/coresignal-pricing).
- Company data: OpenCorporates £2,250 / £6,600 / £12,000 per year [S] — [OpenCorporates](https://opencorporates.com/pricing/).
- Pricing data: Prisync $59-$399/month; Price2Spy $19.95-$67.95 entry [S] — [Capterra](https://www.capterra.com/p/153451/Prisync/pricing/), [xpay](https://www.xpay.sh/saas-pricing/price2spy/).
- Distribution take rates: RapidAPI 25%, Apify 20% plus compute [S] — [RapidAPI](https://docs.rapidapi.com/docs/payouts-and-finance), [Apify](https://docs.apify.com/actors/monetize.md).

### Inferences
- The price gap between raw records (cents per thousand) and a workflow product (alerts, matching, documents, history: $50-£120/user/month) is where value-added margin sits; raw scraping alone is a commodity.
- Pharma data has the highest price points and the most quote-only incumbents, suggesting room underneath for a transparent-priced regional product — but no demand evidence specific to Morocco/Maghreb was found.

### Gaps
- No public prices or products found for Moroccan/Maghreb tender, drug-registration, drug-price or shortage data; local demand is unproven here.
- Licensing terms for re-selling official registry or tender data (each source's reuse conditions) were not reviewed and determine legality.
- TendersInfo, TenderNed, Datarade marketplace fees and AWS Data Exchange terms not retrieved.

---

## Q5. How AI / vibe coding changed competition and defensibility

### Takeaway
Building is no longer a barrier (2,713 Shopify apps launched in one month), distribution and retention are, and cheap AI-wrapper products churn catastrophically. What resists "the customer just uses ChatGPT/Claude" is something the chat window lacks: fresh proprietary data, integration inside a system of record, scheduled unattended operation, and higher-priced B2B workflows.

### Cited Findings
- Supply shock: 2,713 Shopify apps launched in May 2026 alone (21,509 live) [S] — [BigIdeasDB](https://bigideasdb.com/shopify-app-vs-wordpress-plugin); Apify catalog at 25,787 actors [S] — [SignalCensus](https://signalcensus.pages.dev/articles/apify-store-may-2026-25787-actors-480k-mau).
- Retention: AI-native products under $50/month have median GRR 23% / NRR 32%; over $250/month GRR 70% / NRR 85%; overall AI-native GRR 40% vs B2B SaaS NRR 82% (≈3,500 companies with ≥$250k ARR, 2025; buckets ~50 companies, "directional") [V] — [ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/).
- Pieter Levels is reported as saying indie revenue and traffic are declining, including on his own projects, because large AI platforms absorb use cases; Jon Yongfook reported Google referrals roughly halved in 2026 [S, secondary reports] — [Cipher Projects](https://www.cipherprojects.com/blog/posts/ai-killing-indie-hackers-channel-shift-2026/), [Level Up Coding](https://levelup.gitconnected.com/one-of-the-most-successful-indie-hackers-says-ai-killed-the-playbook-716f27f995ec).
- Content/SEO channel erosion: Flippa content sales -39% half-on-half; average age of content sites sold rose to 10+ years [V] — [Flippa](https://flippa.com/blog/digital-ma-insights-h1-2026/).
- Opinion pieces converge on "barriers collapsed, the boring layer is the moat" and "validating didn't get faster" [S] — [Indie Hackers](https://www.indiehackers.com/post/vibe-coding-is-quietly-killing-simple-saas-products-the-thing-thats-actually-defensible-isn-t-a-feature-it-s-the-boring-layer-3a785dadf1), [DEV Community](https://dev.to/lmoncany/why-vibe-coding-is-making-the-customer-problem-worse-not-better-5290).

### Inferences
- Programmatic SEO as a primary channel is a weakening bet in 2026; marketplaces with purchase intent (Shopify, Atlassian, Apify) and direct outreach are relatively stronger.
- A product an agent can build in a week can be cloned in a week; durable advantage for an agent-run solo business is operational (data freshness, coverage, reliability over months) rather than code.
- Pricing under $50/month for an AI feature set selects for tourists; fewer customers at $100-300/month with annual billing is the retention-consistent design.

### Gaps
- Levels' statement was not read at the primary source. No quantified measurement of how many customers replaced a micro-SaaS with a general assistant.

---

## Q6. Benchmarks for low-ticket self-serve SaaS (CAC, churn, conversion)

### Takeaway
Plan on 3-5% free-to-paid for freemium, monthly churn above 3.5% at sub-$100 ARPA, and CAC in the hundreds of dollars if acquisition is paid — which makes paid acquisition uneconomic for low-ticket products and forces marketplace or organic channels.

### Cited Findings
- Freemium conversion: median free-to-paid 8% across products, but bimodal — 25% of freemium products convert below 2.5%; 3-5% is "good", 8-12% "great" for freemium self-serve [S] — [ChartMogul Conversion Report](https://chartmogul.com/reports/saas-conversion-report/).
- First Page Sage (80+ clients, 2021-2025): average freemium-to-paid 3.7% [S] — [Userpilot summary](https://userpilot.com/blog/freemium-saas/). Trial figures conflict across sources: opt-in 18-25%, opt-out 31-60% (different denominators) [S] — [Fungies](https://fungies.io/saas-free-trial-vs-freemium-2026), [Visionary Marketing](https://visionary-marketing.co.uk/blog/saas-free-trial-conversion-statistics-2026).
- Churn targets: ARPA under $100 → aim for monthly churn below 3.5%; over $100 → below 2.5% [S] — [ChartMogul](https://chartmogul.com/lp/saas-churn). An unverified third-party figure puts sub-$25 ARPA at 8.2% gross monthly MRR churn [S] — [Rocking Web](https://rockingweb.pages.dev/saas-metrics-benchmark-report-2025).
- Net retention: median B2B SaaS NRR 82% (upper quartile 97%); B2C SaaS 49%; annual plans +10-20 points [V] — [ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/).
- CAC (vendor blogs, weak): self-serve/PLG median ~$702 (IQR ~$150-$1,200), other pages say $100-$500; payback estimates range from under 6 to 8-11 months [S] — [Saas Hero](https://www.saashero.net/strategy/stripe-cac-benchmarks-b2b-saas/), [Saas Hero CAC 2026](https://www.saashero.net/strategy/saas-cac-benchmarks-2026/).

### Inferences
- At $20/month and 5% monthly churn, lifetime revenue is ~$400 per customer, below the cited median self-serve CAC; low-ticket products only work with near-zero-CAC distribution.
- At 3-5% free-to-paid, 100 paying customers require roughly 2,000-3,300 active free users — a traffic problem before it is a product problem.

### Gaps
- No primary benchmark specifically for sub-$1k ACV solo-run products; OpenView, SaaS Capital, Baremetrics and ProfitWell primary reports were not retrieved. CAC figures above come from a single agency blog and should not be quoted as authoritative.
