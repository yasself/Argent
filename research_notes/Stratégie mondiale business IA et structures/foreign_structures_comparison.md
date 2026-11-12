# Foreign company structures for a non-resident (Moroccan national/resident) founder running global digital businesses — jurisdiction-side comparison (as of 12 Nov 2026)

Reading conventions used throughout:
- **[V]** = verified this session on the linked page (official page fetched, or several concordant professional sources). **[S]** = secondary/marketing source only (reseller, formation agent, blog) — treat as indicative. **[BK]** = researcher background knowledge NOT re-verified this session; listed only under "Gaps" or explicitly tagged, with the official URL where it should be checked.
- Scope: the foreign jurisdictions' own rules. Moroccan exchange control (Office des Changes) and Moroccan tax residency of the company/founder are covered by another researcher; they are only flagged here where they change the reading of a foreign rule (place of effective management).
- No nominee-shareholder, straw-man or fake-residency arrangement is proposed anywhere. Where a jurisdiction legally requires a local officer (Singapore resident director, Hong Kong company secretary, Estonia contact person), that is a disclosed statutory role, not concealment of ownership; the founder remains the declared beneficial owner.

## Master comparison table (synthesis of the sections below)

| Structure | 100% non-resident Moroccan owner allowed? | Formation cost (govt + typical) | Steady-state fixed cost/yr (indicative) | Entity-level tax on a no-local-presence digital business | Dividend WHT to Moroccan-resident individual / treaty with Morocco | Stripe | Remote admin |
|---|---|---|---|---|---|---|---|
| US LLC (WY/NM/DE), foreign-owned disregarded entity | Yes, no nationality restriction [V/S] | WY $100, NM $50, DE ~$110 state fee [S]; Stripe Atlas (DE only) $500 [V] | WY $60 report [S]; NM $0 report [S]; DE $300 tax [S]; + registered agent ($100/yr via Atlas [V]) + Form 5472/pro-forma 1120 preparer | 0% US federal IF not engaged in a US trade or business / no ECI — fact-dependent, not a safe harbour; Form 5472 mandatory, $25,000 penalty [V] | Not a dividend (disregarded); US–Morocco treaty exists (15%/10% dividends) [V] but irrelevant if no US-source income | Yes (US listed) [V] | Very high, except 5472 must be faxed/mailed [V] |
| US C-Corp (Delaware, Stripe Atlas) | Yes [V "almost anywhere"] | $500 Atlas [V] | $100 agent [V] + DE franchise tax + federal/state returns (CPA) | 21% federal [BK] | 30% statutory, 15% under US–Morocco treaty for individuals [V treaty rate] | Yes [V] | High |
| UK Ltd | Yes; director ID verification mandatory since 18 Nov 2025 [V] | £100 digital incorporation [V] | £50 confirmation statement [V] + registered office + accounts/CT600 accountant | 19% (<£50k), marginal relief to 25% (>£250k) [V]; UK-incorporated = UK resident | No UK dividend WHT [BK]; UK–Morocco treaty in force (15%/10% caps) [V] | Yes [V] | High |
| Estonia OÜ (e-Residency) | Yes — Morocco NOT on the 10-country exclusion list (page updated 6 Nov 2026) [V] | €265 state fee [V] + e-Residency card fee [BK €150] + provider | Contact person/address €200–400/yr [V] + accounting (Xolo Leap Pro ≈ €129/mo, inferred [S]) | 0% on retained profit; 22/78 on distributions (2026; 24% rise cancelled) [V] | No extra WHT on dividends [BK]; NO Morocco–Estonia treaty in force (signed 2013, absent from in-force lists) [V] | Yes [V] | Very high (fully digital) |
| Ireland Ltd | Possible but needs an EEA-resident director or a bond [BK] | [BK] | High (accountant; audit exemption for small) [BK] | 12.5% trading [BK] only if managed/controlled in Ireland in substance | Treaty with Morocco (10%/6%) [V] | Yes [V] | Medium |
| Bulgaria EOOD / Lithuania UAB / Netherlands BV / Cyprus Ltd | Yes in law [BK]; bank account is the bottleneck | [BK] | [BK] | BG 10% [BK]; LT/NL/CY rates see Gaps | Treaties: Bulgaria 10%/7%, Lithuania 10%/5%, Netherlands 15%/10% [V]; Cyprus — no treaty listed [V] | Yes for all four [V] | Medium |
| UAE free zone (IFZA, Meydan, RAKEZ, SHAMS…) | Yes, 100% foreign ownership | IFZA licence from ≈ AED 12,900 zero-visa; AED 14,900 one-visa package; all-in with visa ≈ AED 22,250+ [S] | Licence renewal ≈ same as licence [S] + CT return + bookkeeping (+ audit if QFZP) | 0% up to AED 375k profit, 9% above [BK-widely cited]; Small Business Relief (revenue ≤ AED 3m) extended to tax periods ending ≤ 31 Dec 2029 by MD 131/2026 [S, multiple]; QFZP 0% is hard for B2C SaaS | No UAE dividend WHT [BK]; UAE–Morocco treaty (10%/5% caps) [V] | Yes [V] | Medium (portal-based, agent-heavy) |
| Hong Kong Ltd | Yes; needs HK-resident company secretary [S] | HK$1,545 e-incorporation + HK$2,350 business registration (from 1 Apr 2026) [S] | Secretary + registered office + mandatory audit [S] | 8.25% on first HK$2m, 16.5% above [V]; offshore claim case-by-case | No HK dividend WHT [BK]; no HK–Morocco treaty listed [V] | Yes [V] | Medium (audit) |
| Singapore Pte Ltd | Yes as shareholder; needs a locally resident director [BK] + resident secretary [S] | [S/BK] | High (nominee/resident director service, secretary, accounting) | 17% headline; start-up exemption 75% of first S$100k + 50% of next S$100k for first 3 YAs; then partial exemption [V/S] | No SG dividend WHT [BK]; Singapore–Morocco treaty (10%/8% caps) [V] | Yes [V] | Medium |
| Georgia LLC (Virtual Zone / International Company) | Yes [S] | Low [S] | Low [S] | VZP: 0% profit tax only on IT created IN Georgia and supplied abroad; ICS 5% [S, conflicting] | 5% Georgian dividend WHT [S]; no Georgia–Morocco treaty listed [V] | NOT available (Georgia not listed) [V] | Low-medium |

## KQ1 — Can a non-resident Moroccan individual form and own 100%? Nationality restrictions / enhanced due diligence (FATF status)

### Takeaway
No jurisdiction reviewed bars a Moroccan national or resident from owning 100% of a company; the only nationality-based gate checked (Estonia e-Residency) does not list Morocco as of 6 Nov 2026. The practical filter is KYC at banks/EMIs/payment processors, not company law — Morocco is no longer on the FATF grey list, but Stripe does not support Morocco as a business location, which is precisely why a foreign entity is needed.

### Cited Findings
- Estonia e-Residency: applications are not reviewed from citizens of 10 countries — Afghanistan, Burkina Faso, Iran, Yemen, DR Congo, North Korea, South Sudan, Mali, Nigeria, Syria — plus first-time applications from Russian and Belarusian citizens. **Morocco is not on the list.** Article `updated_at` 2026-11-06. — [e-Residency Knowledge Base, "Restrictions on e-Residency applications" (JSON API of the official article)](https://learn.e-resident.gov.ee/api/v2/help_center/articles/4575271559441.json); human-readable page: [learn.e-resident.gov.ee](https://learn.e-resident.gov.ee/hc/en-gb/articles/4575271559441) (returned HTTP 403 to the fetcher, content read via the API endpoint)
- Estonia's e-Residency guidance on bank accounts notes that "if you are a resident of a country on the FATF list of high-risk and other monitored jurisdictions, the criteria are different" (search-snippet only, not opened) — [learn.e-resident.gov.ee](https://learn.e-resident.gov.ee/hc/en-gb/articles/360000625078)
- Stripe Atlas: "Apply online from almost anywhere in the world"; no public country exclusion list on the product page — [stripe.com/atlas](https://stripe.com/atlas)
- UK: from 18 Nov 2025 identity verification is a legal requirement for directors and PSCs; a company cannot be incorporated on/after that date unless the first directors have verified; verification can be done online, at a Post Office or through an authorised agent (ACSP) — [GOV.UK press release](https://www.gov.uk/government/news/companies-house-confirms-identity-verification-rollout-from-18-november-2025); [CMS](https://cms.law/en/gbr/legal-updates/economic-crime-and-corporate-transparency-act-2023-identity-verification-became-mandatory-from-18-november-2025); [Marks & Clerk](https://www.marks-clerk.com/insights/latest-insights/102lwtt-uk-companies-house-id-verification-now-legal-requirement-for-directors-and-pscs/)
- FATF, 30 Oct 2026 plenary: DR Congo, Monaco, Bulgaria and Côte d'Ivoire removed; 18 jurisdictions remain under increased monitoring; no additions; black list unchanged. Names seen in the (truncated) secondary lists — Angola, Bolivia, Bosnia and Herzegovina, Cameroon, Haiti, Iraq, Kenya, Kuwait, Lao PDR, Lebanon, Nepal, Papua New Guinea, South Sudan, Syria — do not include Morocco, but the full 18-name list was not retrieved. — [FATF "Jurisdictions under Increased Monitoring – 30 October 2026"](https://www.fatf-gafi.org/en/publications/High-risk-and-other-monitored-jurisdictions/increased-monitoring-october-2026.html); [FATF plenary outcomes Oct 2026](https://www.fatf-gafi.org/en/publications/Fatfgeneral/outcomes-fatf-plenary-october-2026.html)
- Stripe business-location list (51 countries) includes US, UK, Ireland, Estonia, Bulgaria, Cyprus, Lithuania, Netherlands, UAE, Hong Kong, Singapore; **Morocco and Georgia are not listed** — [stripe.com/global](https://stripe.com/global)
- Hong Kong: company secretary is mandatory and must be an HK-resident individual or HK-registered corporate service company; "no resident director obligation" — [3E Accounting SG-vs-HK 2026 comparison](https://www.3ecpa.com.sg/blog/company-incorporation-in-singapore-vs-hong-kong-2026-comparison/) [S]
- Singapore: company secretary must be ordinarily resident, appointed within 6 months — same source [S]
- Georgia: a single-founder company can obtain Virtual Zone status, but "the developer must create the IT product within Georgia and deliver it abroad" — [Andersen Georgia](https://ge.andersen.com/virtual-zone-person-georgia/); [PB Services](https://pbservices.ge/blog/georgia-it-virtual-zone-tax-benefits/) [S]

### Inferences
- With Morocco off the FATF grey list and absent from the Estonian exclusion list, a Moroccan founder is treated as an ordinary non-EU applicant: standard (not statutory enhanced) due diligence, but individual banks/EMIs apply their own country-risk appetite. Eligibility to form the company is therefore almost never the issue; opening the payment/banking stack is.
- The US LLC, UK Ltd and Estonian OÜ can be formed 100% remotely with no local officer. Singapore (resident director), Hong Kong (resident secretary), Ireland (EEA director or bond) and Estonia (contact person, because management is outside Estonia) each require a paid local statutory role — a disclosed service, not hidden ownership.
- Georgia's Virtual Zone regime is functionally unavailable to a founder who does the development work from Morocco (work must be performed in Georgia) and Georgia is not a Stripe country — it can be dropped from the shortlist unless the founder relocates.

### Gaps
- Morocco's removal from the FATF grey list in Feb 2023 was given in the brief and is consistent with what was found, but the FATF Feb-2023 statement was not re-fetched; check [FATF Feb 2023 increased-monitoring page](https://www.fatf-gafi.org/en/publications/High-risk-and-other-monitored-jurisdictions/Increased-monitoring-february-2023.html) [BK]. The complete Oct 2026 list of 18 names was truncated in results — confirm Morocco's absence on the FATF page directly.
- EU list of high-risk third countries (Delegated Regulation (EU) 2016/1675 as amended): Morocco's current status not verified this session.
- e-Residency practicalities for a Morocco-based applicant: state fee [BK: €150 since 2025] and — importantly — the pickup location. I found no confirmation of a pickup point in Morocco; the card normally must be collected in person at an Estonian embassy or designated pickup point, which may imply a Schengen-visa trip (e.g. Madrid/Lisbon/Paris). Check [e-resident.gov.ee pickup locations](https://www.e-resident.gov.ee/become-an-e-resident/).
- ACRA's rule that a Singapore company needs at least one director ordinarily resident in Singapore was not confirmed on an official page this session [BK; check acra.gov.sg]. Ireland's EEA-resident-director-or-bond (Companies Act 2014 s.137) rule likewise [BK].
- Whether Stripe Atlas, doola, Firstbase or state registered agents apply any Morocco-specific restriction: no source found.
- UAE free-zone nationality screening: free zones run security/immigration screening per nationality for visas; no official source found on Moroccan nationals (anecdotally unrestricted) — unverified.

## KQ2 — Formation cost and realistic annual running cost

### Takeaway
Government fees are trivial everywhere except the UAE (licence ≈ AED 13–22k/yr); the real annual cost is professional compliance (US Form 5472 preparer, UK/Estonia/HK/SG accountants, HK audit, SG resident director). Cheapest credible steady state: US LLC in New Mexico/Wyoming (a few hundred USD/yr) and Estonia OÜ or UK Ltd (roughly €1.5–2.5k/yr with accounting); most expensive: Singapore, Hong Kong and UAE-with-visa.

### Cited Findings
**United States**
- Stripe Atlas: $500 one-time (state filing fees, next-day Delaware processing, EIN, first-year registered agent); $100/yr registered agent thereafter; forms Delaware C-corp, LLC or subsidiary; tax filing not included — [stripe.com/atlas](https://stripe.com/atlas) [V]
- Wyoming LLC: $100 formation; annual report licence tax $60 minimum, due first day of the anniversary month — [LLC University fee table](https://www.llcuniversity.com/llc-annual-fees-by-state/); [Northwest Registered Agent](https://www.northwestregisteredagent.com/llc/state-annual-fees) [S]
- New Mexico LLC: $50 formation; no annual report (recurring state cost $0) — same sources [S]
- Delaware LLC: ~$110 formation; $300 annual tax due 1 June — same sources [S]; Delaware Division of Corporations fee schedule revised 1 Aug 2026: certificate of incorporation from $109, 24-hour expedite +$50 — reported via [Rho](https://www.rho.co/blog/stripe-atlas-review) [S]
- Form 5472 + pro-forma 1120 cannot be e-filed by a foreign-owned DE; must be faxed (855-887-7737) or mailed to Ogden, UT — [IRS Instructions for Form 5472 (Rev. 12/2024; page reviewed 30 Apr 2026)](https://www.irs.gov/instructions/i5472) [V]

**United Kingdom**
- From 1 Feb 2026: digital incorporation £100 (was £50), paper £124; digital confirmation statement £50/yr; voluntary strike-off £13 — [GOV.UK news](https://www.gov.uk/government/news/companies-house-fees-are-changing-from-1-february-2026); [GOV.UK Companies House fees](https://www.gov.uk/government/publications/companies-house-fees/companies-house-fees) [V]

**Estonia**
- Company registration state fee €265 (online, 15 min–1 h); contact person/legal address €200–400/yr from licensed providers; EEA neobank account €0–200 — [e-resident.gov.ee "Start a company"](https://www.e-resident.gov.ee/start-a-company/) [V]
- Xolo Leap Pro promotion "first two months free, saving up to €258" (⇒ ≈ €129/month list price), 6-month minimum commitment — [Xolo help page](https://www.xolo.io/zz-es/faq/xolo-leap/category/promotions/article/leap-pro-2-months-for-free---promotion) [S, undated]

**UAE**
- IFZA: zero-visa licence from AED 12,900 (3 activities, 3 shareholders); published package tiers AED 14,900 (1 visa), 16,900 (2), 18,900 (3); establishment card ≈ AED 2,000 (included in some quotes, separate in others); visa from ≈ AED 3,750 each; typical all-in with one visa ≈ AED 22,250; one reseller quotes AED 37,200 all-in year 1 including its own fee. "IFZA does not publish one single official price." — [Avyanco, updated Jul 2026](https://avyanco.com/ifza-free-zone-cost/); [BusinessDubai](https://www.businessdubai.ae/blogs/ifza-free-zone-setup); [QAS Pro Global, updated 3 Oct 2026](https://qasproglobal.com/ifza-free-zone-dubai-2026/) [S — reseller figures]
- Meydan Free Zone fee page (not opened) — [Avyanco Meydan](https://avyanco.com/meydan-free-zone-cost/) [S]
- Small businesses must still register and file a corporate tax return even when no tax is due — [Gulf News](https://gulfnews.com/business/corporate-tax/uae-reminds-small-businesses-to-file-corporate-tax-returns-even-if-no-tax-is-due-1.500629117)
- QFZP status requires audited financial statements and transfer-pricing documentation — [IFZA QFZP guide (Jan 2026)](https://ifza.com/wp-content/uploads/2026/01/Guide-to-Qualifying-Free-Zone-Persons-QFZPs-in-the-UAE-1.pdf); [Middle East Briefing](https://www.middleeastbriefing.com/news/understanding-uaes-new-free-zone-tax-regulations/)

**Hong Kong / Singapore**
- Hong Kong: HK$1,545 electronic incorporation + HK$2,350 one-year Business Registration Certificate (registrations from 1 Apr 2026); annual audited financial statements compulsory; resident company secretary mandatory — [3E Accounting](https://www.3ecpa.com.sg/blog/company-incorporation-in-singapore-vs-hong-kong-2026-comparison/); [private.law wiki](https://wiki.private.law/en/hong-kong-vs-singapore-company) [S]
- Singapore: resident company secretary within 6 months — same [S]

### Inferences
- Indicative total cost of ownership, fixed costs only (ranges are researcher estimates combining the cited government fees with typical market prices for accounting; the accounting components are NOT sourced and must be re-quoted):
  - US LLC (NM/WY, DIY agent): Year 1 ≈ $300–1,000; steady ≈ $300–900/yr (state $0–60 + agent ≈ $50–150 + 5472/1120 preparer). Via Stripe Atlas (Delaware LLC): Year 1 $500 + preparer; steady $100 agent + $300 DE tax + preparer ≈ $700–1,200.
  - Delaware C-Corp via Atlas: Year 1 $500 + CPA; steady $100 agent + DE franchise tax/annual report + federal 1120 by CPA ≈ $1,500–3,000+.
  - UK Ltd: Year 1 £100 + registered-office service + accountant; steady £50 + address + accounts/CT600 ≈ £800–2,000.
  - Estonia OÜ: Year 1 ≈ €265 + e-Residency fee + provider (≈ €1,500–2,500 with a Xolo-type plan); steady ≈ €1,500–2,300 (≈ €129/mo all-in plan, or €200–400 contact person + separate accountant).
  - UAE free zone: zero-visa ≈ AED 13–15k/yr (≈ $3.5–4k) + bookkeeping/CT filing; with one investor visa Year 1 ≈ AED 22–37k (≈ $6–10k) and renewals at roughly licence level plus visa renewal every 2–3 years.
  - Hong Kong: materially higher because of mandatory audit + secretary (commonly quoted in the low-to-mid thousands USD/yr; not sourced).
  - Singapore: highest of the "mainstream" set because a resident-director service is needed on top of secretary and accounting (not sourced).
- New Mexico is the lowest-cost US state on paper (no annual report), Wyoming is the usual compromise (cheap, well-served by agents), Delaware only makes sense if using Atlas or planning a C-corp/VC path.

### Gaps
- Official state fee pages (Wyoming SOS, New Mexico SOS, Delaware Division of Corporations) were not fetched directly; figures come from formation-industry tables. Verify at sos.wyo.gov, sos.nm.gov, corp.delaware.gov. Delaware C-corp minimum franchise tax ($175 + $50 annual report under the authorized-shares method) is [BK].
- doola, Firstbase, 1Office, Companio, Xolo list prices for 2026: no usable source retrieved (Xolo pricing URL returned 404; search returned nothing for the others). The ≈ €129/month Xolo Leap Pro figure is an inference from a promotion page.
- Prices of US Form 5472 preparation ($150–600 is commonly advertised) — no source retrieved.
- Official price lists for RAKEZ, Meydan, SHAMS, DMCC, Dubai Internet City, ADGM, DIFC and mainland licences were not retrieved. General market knowledge [BK]: SHAMS/RAKEZ/Meydan/IFZA are the low-cost tier; DMCC, Dubai Internet City, ADGM and DIFC cost several times more and require real office space; none of this was verified this session.
- Singapore nominee/resident director service cost, Hong Kong audit cost, Ireland/Netherlands/Cyprus/Bulgaria/Lithuania formation and running costs: not sourced.
- Estonia minimum share capital (reformed to €0.01 minimum in 2023) and e-Residency state fee (€150 from 2025) are [BK]; the official start-a-company page fetched did not state them.

## KQ3 — Corporate tax actually applicable (digital business, no local presence, foreign owner)

### Takeaway
At entity level the realistic ranking is: US foreign-owned LLC 0% federal (conditional, and it merely pushes all taxation to the owner's country), UAE 0% in practice for small businesses (Small Business Relief now runs to 2029; otherwise 0%/9% with a AED 375k band), Estonia 0% until distribution then 22%, Hong Kong 8.25%/16.5%, Singapore ≈ 4–12% effective at these profit levels, UK 19–25%, US C-corp 21% plus 15% treaty dividend withholding. Every "0%" depends on conditions the founder's facts must actually meet, and none of them says anything about Moroccan tax.

### Cited Findings
**US LLC (single-member, foreign-owned, disregarded)**
- A foreign person generally must be engaged in a US trade or business for income to be ECI; performing personal services in the US generally constitutes a US trade or business if activities are "considerable, continuous and regular"; ECI is taxed at graduated rates after deductions — [IRS, "Effectively Connected Income (ECI)", updated 18 Aug 2026](https://www.irs.gov/individuals/international-taxpayers/effectively-connected-income-eci) [V]
- A foreign-owned US DE "has no income tax return requirement" as such but must file a pro-forma Form 1120 with Form 5472 attached when it has reportable transactions with its foreign owner/related parties (including formation, contributions and distributions); penalty $25,000 for failure to file timely/completely or to keep records, plus $25,000 per 30 days after 90 days from IRS notice; due with Form 1120 deadline, extendable by Form 7004 — [IRS Instructions for Form 5472](https://www.irs.gov/instructions/i5472) [V]
- Practitioner commentary: a dependent agent in the US (working exclusively/almost exclusively for the company, regular, substantial and continuous activity; independent-agent exception in Treas. Reg. §1.864-7(d)) is the usual ETBUS trigger; one practitioner warns ETBUS can exist with zero US dependent agents; a practitioner memo says SaaS sold to US customers from abroad with all servers and personnel abroad "is not typically a US trade or business", while US-based servers or support staff "complicates the analysis" — [Online Taxman](https://onlinetaxman.com/us-llc-tax-haven-for-foreigners/); [terms.law memo](https://terms.law/insights/us-tax-exposure-asia-founders-selling-us.html); [terms.law 2024](https://terms.law/2024/12/05/how-the-irs-taxes-foreign-owned-u-s-entities-selling-online/) [S — practitioner opinion, not authority]
- BOI/Corporate Transparency Act: FinCEN final rule issued 11 Aug 2026, effective 14 Aug 2026, permanently adopts the March 2025 interim final rule — entities formed in the US ("domestic reporting companies") are exempt from BOI reporting; only foreign-formed entities registered to do business in a US state still report (and not for US-person owners). One firm notes constitutional litigation is not entirely over. — [Ballard Spahr](https://www.ballardspahr.com/insights/alerts-and-articles/2026/08/fincen-permanently-exempts-us-entities-and-persons-from-beneficial-ownership-reporting); [Morrison Foerster](https://www.mofo.com/resources/insights/260820-fincen-ends-beneficial-ownership-reporting); [ABA Washington Letter](https://www.americanbar.org/advocacy/governmental_legislative_work/publications/washingtonletter/august-26-wl/cta-beneficial-ownership-reporting-0826wl/); [Troutman](https://www.troutman.com/insights/relief-is-real-but-not-universal-fincen-permanently-ends-boi-reporting-for-us-companies/) [V via multiple law-firm alerts; Federal Register text not opened]

**US C-Corp**
- US–Morocco treaty: reciprocal maximum source tax of 15% on portfolio dividends, 10% to parent companies — [IRS treaty document (archived)](https://webarchive.library.unt.edu/eot2008/20090115092228/http://www.irs.gov/pub/irs-trty/morocco.pdf); consistent with [PwC Morocco WHT table, reviewed 30 Apr 2026](https://taxsummaries.pwc.com/morocco/corporate/withholding-taxes) [V]

**UK**
- Financial years from 1 Apr 2025 and 2026: small profits rate 19% (profits < £50,000), main rate 25% (> £250,000), marginal relief in between with standard fraction 3/200 — [GOV.UK Corporation Tax rates and allowances](https://www.gov.uk/government/publications/rates-and-allowances-corporation-tax/rates-and-allowances-corporation-tax) [V]

**Estonia**
- 2026 CIT: 22% (22/78 of the net distribution); 0% on retained/reinvested profit; the planned rise to 24% and the 2% defence/security levy on profits were abolished (Riigikogu, 19 Jun 2025; further amendments Dec 2025) — [KPMG Estonia 2026 Tax Card](https://assets.kpmg.com/content/dam/kpmgsites/ee/pdf/tax-cards/2026%20Tax%20Card-web.pdf.coredownload.inline.pdf); [EY Tax Alert 9 Jul 2025](https://taxnews.ey.com/news/2025-1409-estonia-abolishes-temporary-defense-tax-increases-several-tax-rates); [PwC Estonia](https://taxsummaries.pwc.com/estonia/corporate/taxes-on-corporate-income); [1Office](https://1office.co/blog/estonia-tax-changes-2026/) [V]. Note: older pages (e.g. Bloomberg Tax) still state 24% for 2026 — outdated.

**UAE**
- Small Business Relief (taxable income treated as nil; revenue ≤ AED 3m in the period and all prior periods; must be elected in each return; not available to QFZPs, non-residents or large-MNE members; lost permanently once the threshold is exceeded; anti-fragmentation rule) **extended by Ministerial Decision No. 131 of 2026 to tax periods ending on or before 31 Dec 2029** (previously 31 Dec 2026) — [Khaleej Times](https://www.khaleejtimes.com/business/uae-extends-corporate-tax-relief-for-small-businesses-until-2029); [Entrepreneur ME](https://mena.entrepreneur.com/business-news/uae-extends-small-business-tax-relief-through-2029); [Grant Thornton UAE](https://www.grantthornton.ae/insights/alerts/recent-uae-and-regional-tax-updates/); [Orbitax](https://orbitax.com/news/country/article/UAE-Small-Business-Relief-for--62798) [V via multiple concordant secondary sources; MoF decision text not opened]. Some reseller pages still say "2026 last chance" — outdated.
- QFZP 0% regime: governed by Cabinet Decision 100 of 2023 + Ministerial Decision 229 of 2025 (qualifying/excluded activities, reported as retroactive to 1 Jun 2023); requires adequate substance in the free zone, qualifying income, audited accounts, transfer-pricing compliance and non-qualifying revenue ≤ the lower of 5% of revenue or AED 5m — [IFZA QFZP guide](https://ifza.com/wp-content/uploads/2026/01/Guide-to-Qualifying-Free-Zone-Persons-QFZPs-in-the-UAE-1.pdf); [Middle East Briefing](https://www.middleeastbriefing.com/news/understanding-uaes-new-free-zone-tax-regulations/); [BSA Law](https://bsalaw.com/insight/uae-tax-updates-august-2025/) [S/V]

**Hong Kong**
- Two-tier profits tax: 8.25% on the first HK$2m of assessable profits of a corporation, 16.5% above; only one connected entity may elect — [IRD FAQ](https://www.ird.gov.hk/eng/faq/2tr.htm) [V]

**Singapore**
- Headline 17%; start-up exemption (first 3 YAs): 75% of first S$100,000 + 50% of next S$100,000 exempt (max S$125,000); thereafter partial exemption 75% of first S$10,000 + 50% of next S$190,000 — [IRAS corporate tax rates](https://www.iras.gov.sg/irashome/Quick-Links/Tax-Rates/Corporate-Tax-Rates/) (surfaced in search, summary from concordant secondary sources: [3E Accounting](https://www.3ecpa.com.sg/blog/singapore-corporate-tax-exemptions-for-startups-updated-2026/), [SingaporeLegalAdvice](https://singaporelegaladvice.com/law-articles/start-up-tax-exemption-singapore-companies/))

**Georgia**
- Virtual Zone Person: 0% profit tax only on profit from IT created in Georgia and supplied outside Georgia; 5% dividend withholding; International Company status reported as 5% profit tax (one source: 5% profit / 5% payroll / 0% dividend — sources conflict) — [Andersen Georgia](https://ge.andersen.com/virtual-zone-person-georgia/); [PwC Georgia incentives](https://taxsummaries.pwc.com/Georgia/Corporate/Tax-credits-and-incentives); [IBCCS](https://ibccs.tax/?p=23357) [S]

### Inferences
- **Entity-level tax on profit of USD 20k / 100k / 300k (researcher calculations from the cited rates; FX assumptions: 1 USD = 3.6725 AED, 7.8 HKD, ≈1.30 SGD, 1 GBP ≈ 1.30 USD — assumptions, not sourced):**

| Structure | 20k | 100k | 300k | Notes |
|---|---|---|---|---|
| US LLC, no ETBUS/ECI | $0 | $0 | $0 | Conditional; all income then taxable only where the owner is tax-resident |
| US C-Corp (21% federal) | $4,200 (21%) | $21,000 (21%) | $63,000 (21%) | If fully distributed with 15% treaty WHT: combined ≈ 32.9% |
| UK Ltd | ≈ $3,800 (19%) | ≈ $21,600 (≈ 21.6%) | ≈ $74,600 (≈ 24.9%) | £15.4k / £76.9k / £230.8k with marginal relief |
| Estonia OÜ — retained | $0 | $0 | $0 | Tax deferred, not eliminated |
| Estonia OÜ — fully distributed | $4,400 (22%) | $22,000 (22%) | $66,000 (22%) | 22/78 of net dividend |
| UAE, Small Business Relief elected (revenue ≤ AED 3m ≈ $817k) | $0 | $0 | $0 | Through tax periods ending ≤ 31 Dec 2029 |
| UAE, standard regime (0% to AED 375k, 9% above) | $0 | $0 (AED 367k is just under the band) | ≈ $17,800 (≈ 5.9%) | [BK band, widely cited] |
| Hong Kong (onshore) | $1,650 (8.25%) | $8,250 (8.25%) | ≈ $28,400 (≈ 9.5%) | Offshore claim could reduce to 0 but is audited case by case |
| Singapore, first 3 YAs | ≈ $850 (4.3%) | ≈ $5,200 (5.2%) | ≈ $34,700 (11.6%) | |
| Singapore, after year 3 | ≈ $1,400 (6.9%) | ≈ $8,200 (8.2%) | ≈ $37,600 (12.5%) | |

- **US LLC uncertainty, stated plainly:** the "0% US tax" result is not an exemption written anywhere; it is the consequence of (a) the LLC being disregarded, so the taxpayer is the foreign individual, and (b) that individual having no US trade or business / no US-source ECI. For a solo founder doing all work from Morocco with no US employees, office or dependent agent, the conventional practitioner view is no ETBUS. Residual uncertainties: (i) characterization and sourcing of SaaS/data-subscription income (service vs. licence/royalty — US-source royalties could be FDAP subject to 30% withholding, reduced by the US–Morocco treaty); (ii) use of US contractors/fulfilment agents who look "dependent"; (iii) the IRS has issued no SaaS-specific guidance in the sources found. This needs a US cross-border tax opinion if US customers are material.
- The disregarded LLC is fiscally transparent: it gives no deferral and no "foreign company" shield for home-country purposes — 100% of profit is the founder's income in the year earned. Conversely, Estonia is the only option reviewed offering genuine indefinite deferral at entity level.
- A foreign-owned disregarded LLC is generally not a treaty "resident" of the US (it pays no US tax), so it cannot obtain a US residency certificate (Form 6166) for itself; treaty benefits, if any, run through the Moroccan owner. [Inference from the disregarded status; not separately sourced.]
- **UAE:** a typical B2C/B2B SaaS selling to worldwide customers will usually NOT fit QFZP (income from natural persons and most non-listed service activities are non-qualifying; audit + substance required). The realistic UAE path for a small digital business is ordinary 9% regime + Small Business Relief (0% until revenue exceeds AED 3m, now to 2029), then 9% above AED 375k. Note SBR is revenue-based: a business with $300k profit almost certainly has revenue under $817k only if margins are high — check.
- **UK:** highest entity tax of the set and no deferral; attractive only for credibility, Stripe/banking access and the treaty.
- **US sales tax / EU VAT:** these follow the customer, not the entity. Any structure selling SaaS to US consumers faces state economic-nexus thresholds (commonly $100k sales per state [BK]) and any structure selling B2C digital services into the EU must charge destination VAT via the non-Union OSS (or Union OSS for an EU entity) [BK]. A merchant-of-record (Paddle, Lemon Squeezy, Polar, Dodo) removes this burden; not verified this session.

### Gaps
- UAE 9% rate/AED 375,000 band and 5% VAT (mandatory registration threshold AED 375,000 of UAE taxable supplies) were not re-verified on tax.gov.ae/mof.gov.ae this session [BK — check [MoF corporate tax page](https://mof.gov.ae/corporate-tax/)]. The text of Ministerial Decision 131 of 2026 was not opened.
- Whether SaaS/data subscriptions fall inside any QFZP "qualifying activity" under MD 229/2025: no source addresses it directly; my reading (they do not) is an inference.
- US federal 21% rate, 30% statutory dividend withholding, Delaware's non-taxation of income of companies not operating in Delaware, and absence of state income tax in Wyoming are [BK], not re-verified.
- Hong Kong offshore-profits claim procedure (DIPN 21) and its success conditions for a founder working from Morocco: not researched; also HK's FSIE regime. Not verified.
- Ireland (12.5% trading rate), Netherlands (19%/25.8%), Bulgaria (10% CIT, dividend tax 5% — a 2026 budget proposal to raise it to 10% was reported as withdrawn), Lithuania (CIT raised to 17% in 2026; reduced small-company rate), Cyprus (CIT raised from 12.5% to 15% from 1 Jan 2026 under the tax reform): all [BK], none verified this session — treat as leads only.
- Georgia International Company status: conflicting descriptions; official rs.ge / mof.ge text not checked.
- US state sales-tax economic nexus thresholds and EU OSS obligations: not sourced this session.

## KQ4 — Substance requirements and "place of effective management" (PoEM) risk

### Takeaway
Every foreign company run single-handedly from Morocco has its mind and management in Morocco; the foreign jurisdiction will still tax it by incorporation (UK, Estonia, UAE, Singapore-if-controlled-there, HK on HK-source profits), so the PoEM risk is a risk of *additional* Moroccan taxation, not a defence against foreign tax. Only regimes with explicit substance tests (UAE QFZP, Georgia Virtual Zone, HK offshore claim, Singapore tax residency/treaty access) are directly undermined on the foreign side.

### Cited Findings
- UAE QFZP requires "adequate substance" in the free zone, audited financial statements and TP documentation — [IFZA QFZP guide](https://ifza.com/wp-content/uploads/2026/01/Guide-to-Qualifying-Free-Zone-Persons-QFZPs-in-the-UAE-1.pdf); [Middle East Briefing](https://www.middleeastbriefing.com/news/understanding-uaes-new-free-zone-tax-regulations/)
- UAE Small Business Relief is available only to a UAE *resident* person; non-resident persons are not eligible — [Virtuzone](https://virtuzone.com/blog/uae-corporate-tax-small-business-relief/); [Osome](https://osome.com/ae/blog/small-business-relief-extended-2029/) [S]
- Georgia Virtual Zone: IT product must be created within Georgia — [Andersen Georgia](https://ge.andersen.com/virtual-zone-person-georgia/)
- Estonia: the official e-Residency site frames the "contact person or legal address" (€200–400/yr) as the standing requirement for companies run from abroad — [e-resident.gov.ee](https://www.e-resident.gov.ee/start-a-company/)
- US: ETBUS depends on activities in the US; a foreign-owned DE with none still has the Form 5472 duty — [IRS ECI page](https://www.irs.gov/individuals/international-taxpayers/effectively-connected-income-eci); [IRS i5472](https://www.irs.gov/instructions/i5472)
- Morocco's treaties (65 in force per OECD peer review) are being modified by the MLI, which Morocco signed in 2019 — [OECD peer review on treaty shopping, Morocco](https://www.oecd.org/en/publications/prevention-of-tax-treaty-abuse-sixth-peer-review-report-on-treaty-shopping_36cebf8e-en/full-report/morocco_f1139177.html); [Upsilon Consulting](https://upsilon-consulting.com/en/tax-treaties-morocco/) [S]

### Inferences
- Where a treaty with Morocco exists (US, UK, UAE, Ireland, Singapore, Netherlands, Bulgaria, Lithuania), a company treated as resident in both states falls under the treaty's dual-residence tie-breaker (historically PoEM; under MLI Art. 4 where applicable, mutual agreement, with treaty benefits denied until agreed). A solo founder in Morocco would lose a PoEM tie-break on the facts. Where no treaty exists (Estonia, Hong Kong, Cyprus, Georgia), there is no tie-breaker at all: double taxation is relieved only by domestic law.
- UAE company incorporated in a free zone is UAE-resident by incorporation for UAE CT, so SBR is available on the UAE side even with the owner abroad [inference]; but a UAE Tax Residency Certificate for treaty purposes and bank-level substance scrutiny (office lease/flexi-desk, UAE-resident manager) are separate hurdles.
- The US disregarded LLC sidesteps PoEM on the foreign side entirely (there is no US corporate taxpayer), which is why it is the least "fragile" structure legally — at the price of full, immediate transparency to the owner's home tax system.
- The UAE Economic Substance Regulations were, to my knowledge, withdrawn for financial years after 31 Dec 2022 once corporate tax arrived [BK — not verified]; substance now matters via QFZP, TRC and banking rather than ESR filings.
- Honest structuring implication: unless the founder actually relocates (e.g. to the UAE), the choice of foreign entity should be made on payments access, compliance cost and credibility, assuming the profits are fully declarable where the founder lives; a design that only works if the home country never looks through it is not robust.

### Gaps
- HMRC manual INTM120060 (central management and control) and the UK position on UK-incorporated companies managed abroad were not fetched. [BK: a UK-incorporated company is UK-resident by incorporation (CTA 2009 s.14) unless a treaty tie-breaker assigns it elsewhere (s.18).]
- Estonia's rule on companies whose management board is abroad (Commercial Code contact-person requirement) not checked against the statute; nor Estonia's stance on a PE of the OÜ arising abroad.
- Singapore: tax residence depends on where control and management is exercised (board meetings) — IRAS will typically not issue a certificate of residence to a company managed from abroad with only a nominee local director [BK, not verified]; the SUTE exemption itself is believed to be available regardless of residence but this was not confirmed.
- Withdrawal of UAE ESR (Cabinet Decision 98 of 2024) not verified this session.

## KQ5 — Residence rights from owning the company; UAE visa and tax-residency-certificate conditions; licence cost with/without visa

### Takeaway
Among the options, only the UAE gives the owner a residence permit as a by-product (investor/partner visa attached to the licence); US, UK, Estonia (e-Residency is expressly not residency), Hong Kong and Singapore companies confer no right to live there. UAE individual tax residency requires 183 days, or 90 days plus a valid residence permit and a UAE home or job/business — a visa alone is not tax residency.

### Cited Findings
- UAE individual tax residence (Cabinet Decision 85 of 2022, effective 1 Mar 2023; Ministerial Decision 27 of 2023): (i) usual/primary residence and centre of financial and personal interests in the UAE; or (ii) ≥ 183 days physical presence in a consecutive 12-month period; or (iii) ≥ 90 days in 12 months AND UAE/GCC national or holder of a valid UAE residence permit AND a permanent place of residence in the UAE or employment/business in the UAE. Any part of a day counts; days need not be consecutive. TRC applied for online via the FTA — [EY, 22 Mar 2023](https://taxnews.ey.com/news/2023-0539-uae-issues-additional-guidance-on-determination-of-tax-residency-for-individuals); [PwC ME](https://www.pwc.com/m1/en/tax/documents/2023/uae-tax-residence.pdf); [Rödl](https://www.roedl.com/insights/uae-determination-tax-residency); [Crowe UAE](https://crowe.com/ae/news/uae-tax-residency-rules-interaction-with-tax-treaties) [V]
- A separate, treaty-specific TRC track under Ministerial Decision 247 of 2023 is described by one secondary source — [private.law wiki](https://wiki.private.law/en/uae-tax-residency) [S, unverified]
- IFZA costs: zero-visa licence ≈ AED 12,900; one-visa licence package AED 14,900; plus establishment card ≈ AED 2,000 and visa processing from ≈ AED 3,750 → typical ≈ AED 22,250 all-in with one visa; reseller all-in quote AED 37,200 — [Avyanco](https://avyanco.com/ifza-free-zone-cost/); [BusinessDubai](https://www.businessdubai.ae/blogs/ifza-free-zone-setup); [Business Link UAE](https://www.businesslinkuae.com/ifza-visa-cost) [S]
- Estonia: e-Residency is a digital identity; restrictions page and programme materials treat it separately from any residence right — [e-Residency KB](https://learn.e-resident.gov.ee/api/v2/help_center/articles/4575271559441.json)

### Inferences
- In USD: UAE free zone without visa ≈ $3.5k/yr; with one visa ≈ $6k (bare) to $10k (reseller all-in) in year 1. The visa adds medical test, Emirates ID and (often) a lease/Ejari if a bank account or TRC is wanted — the true cost of *credible* UAE residency is dominated by housing and the 90/183 days of presence, not the licence.
- A Moroccan founder who keeps home, family and >183 days in Morocco remains Moroccan tax resident whatever UAE visa he holds; the UAE–Morocco treaty tie-breaker (permanent home → centre of vital interests) would point to Morocco [inference; treaty text not opened].
- The UAE route only changes the tax outcome if it is a real relocation. Presented that way it is a legitimate, widely used option; presented as a paper residency it is exactly the "fake residency" pattern excluded by the brief.

### Gaps
- The rule that a UAE residence visa lapses after more than 180 consecutive days outside the UAE (hence "visit every 180 days"), and Golden-visa exemptions from it: not confirmed by any source retrieved this session [BK — check ICP/GDRFA or u.ae].
- Official 2026 fee schedules for investor/partner visas (2-year vs 3-year validity; some zones differ), medical/Emirates ID fees, and refundable deposits: not retrieved.
- Corporate TRC conditions for a free-zone company (commonly: ≥ 1 year of existence, audited accounts, lease, UAE bank statements) not verified.
- Whether any other reviewed jurisdiction offers a founder visa relevant to a Moroccan national (Estonia startup/D-visa, Netherlands self-employed, Georgia stay rules for Moroccans): not researched.

## KQ6 — Dividend withholding to a Moroccan-resident individual and existence of a tax treaty with Morocco

### Takeaway
Morocco has treaties in force with the US, UK, UAE, Ireland, Singapore, Netherlands, Bulgaria, Lithuania, Latvia, Malta, Switzerland, Luxembourg and Canada among others; it has NO treaty in force with Estonia (signed 2013, never appearing in in-force lists), Hong Kong, Cyprus or Georgia. In practice dividend withholding only bites for the US C-corp (30% → 15%) and Georgia (5%); the UK, UAE, Singapore, Hong Kong and Estonia levy no dividend withholding under domestic law.

### Cited Findings
- PwC Morocco WHT table (reviewed 30 Apr 2026) — treaty dividend caps (individuals/portfolio vs qualifying companies): United States 15%/10%; United Kingdom 15%/10%; UAE 10%/5%; Ireland 10%/6%; Singapore 10%/8%; Netherlands 15%/10%; Bulgaria 10%/7%; Lithuania 10%/5%; Latvia 10%/6%; Malta 10%/6.5%; Switzerland 15%/7%; Luxembourg 15%/10%; Canada 15%/10%. **Estonia, Hong Kong, Cyprus and Georgia are absent from the list.** — [PwC Worldwide Tax Summaries, Morocco – Withholding taxes](https://taxsummaries.pwc.com/morocco/corporate/withholding-taxes) [V]. Caveat: the table shows rates on Morocco-source payments; treaty caps are normally reciprocal, but each treaty text should be checked for the reverse direction.
- US–Morocco treaty: "reciprocal maximum rates of tax at source of 15 percent on dividends to portfolio investors, 10 percent on dividends to parent companies" — [IRS treaty document (archived copy)](https://webarchive.library.unt.edu/eot2008/20090115092228/http://www.irs.gov/pub/irs-trty/morocco.pdf); [Freeman Law summary](https://freemanlaw.com/?p=22039)
- Estonia–Morocco: treaty signed 25 Sep 2013 in New York; Estonian government approved it for ratification 28 Aug 2014; no entry into force found — [Orbitax](https://orbitax.com/news/country/article/Treaty-between-Estonia-and-Mor-3753); [ITR, Oct 2013](https://www.internationaltaxreview.com/article/2a69p0gxbfuq19bipt88w/treaties-of-the-week-october-7-2013). Clearstream's list of Estonian treaties in force (updated 31 Dec 2024) does not include Morocco — [Clearstream](https://clearstream.com/clearstream-en/res-library/market-coverage/equities-double-taxation-treaties-concluded-by-estonia-and-currently-in-force-ceu--4233374) [V]
- UAE–Morocco: 1999 convention in force — [Upsilon Consulting](https://upsilon-consulting.com/en/morocco-uae-tax-convention/) [S]
- Georgia: 5% withholding on dividends to shareholders — [Andersen Georgia](https://ge.andersen.com/virtual-zone-person-georgia/) [S]
- Morocco has 65 tax agreements in force per its OECD peer-review response — [OECD](https://www.oecd.org/en/publications/prevention-of-tax-treaty-abuse-sixth-peer-review-report-on-treaty-shopping_36cebf8e-en/full-report/morocco_f1139177.html)
- Treaty benefits generally require a tax-residence certificate from the Moroccan DGI — [Upsilon Consulting](https://upsilon-consulting.com/en/tax-treaties-morocco/) [S]

### Inferences
- Summary for a Moroccan-resident individual shareholder (foreign-side only): US C-corp 15% (treaty; W-8BEN) — and LLC distributions are not dividends at all; UK 0% (no domestic WHT) ; UAE 0%; Singapore 0%; Hong Kong 0%; Estonia 0% WHT beyond the 22/78 company-level charge, but with no treaty the Moroccan side gives no treaty credit mechanism for that corporate tax; Ireland: 25% domestic dividend withholding with a statutory exemption for treaty-country residents on filing a declaration, otherwise capped at 10% [BK]; Netherlands 15% (= treaty cap for individuals) [BK]; Bulgaria 5% domestic [BK]; Georgia 5%, no treaty.
- Absence of a treaty (Estonia, HK, Cyprus, Georgia) matters less for withholding than for (a) the lack of a corporate tie-breaker, and (b) how Morocco classifies/credits the foreign tax — a point for the Moroccan-side researcher.

### Gaps
- The Moroccan DGI's official treaty list (tax.gov.ma) was not fetched; treaty existence relies on PwC + Clearstream + news. Confirm Estonia's non-entry-into-force on [emta.ee](https://www.emta.ee) or the Riigi Teataja, and the absence of HK/Cyprus/Georgia treaties on the DGI list.
- Domestic dividend WHT rates for the UK, UAE, Singapore, HK, Estonia, Ireland, Netherlands, Bulgaria, Cyprus, Lithuania were not individually verified this session [BK].
- Limitation-on-benefits/principal-purpose-test effect of the MLI on these treaties for a one-person company: not analysed.

## KQ7 — Access to Stripe, PayPal Business and business bank/EMI accounts (headline only)

### Takeaway
Stripe onboards businesses by the entity's country: US, UK, Ireland, Estonia, Bulgaria, Cyprus, Lithuania, Netherlands, UAE, Hong Kong and Singapore entities qualify; Moroccan and Georgian entities do not. The US LLC/C-corp via Atlas has the most integrated path (entity + EIN + Stripe account in one flow).

### Cited Findings
- Stripe's country list (51): includes United States, United Kingdom, Ireland, Estonia, Bulgaria, Cyprus, Lithuania, Latvia, Netherlands, Malta, United Arab Emirates, Hong Kong, Singapore; Morocco and Georgia not listed; India and Indonesia "Preview"; Ghana/Kenya/Nigeria/South Africa/Côte d'Ivoire via Paystack "extended network" — [stripe.com/global](https://stripe.com/global) [V]
- Stripe Atlas bundles the tax ID (EIN) and offers a Stripe Treasury-linked account (banking services by Fifth Third Bank; Stripe is not a bank) — [stripe.com/atlas](https://stripe.com/atlas) [V]
- Vendor claims: Moroccan businesses "must set up a US LLC, obtain an EIN, and maintain a US bank account and address to use Stripe" (Dodo Payments); Osome recommends a UK company for Moroccan founders — [Dodo Payments](https://dodopayments.com/blogs/merchant-of-record-morocco); [Osome](https://osome.com/uk/blog/stripe-account-setup-in-morocco) [S — marketing]
- Estonia official guidance: business account at an EEA neobank can be opened fully online, €0–200 — [e-resident.gov.ee](https://www.e-resident.gov.ee/start-a-company/)
- Merchant-of-record providers publish their own supported-country lists for sellers (alternative to owning a Stripe account) — [Polar](https://polar.sh/docs/merchant-of-record/supported-countries); [Creem](https://docs.creem.io/faq/supported-countries) [S, not opened]

### Inferences
- Stripe requires the account's representative/owner to pass identity verification but, per the country model above, the gating criterion is the entity's country plus a local-currency bank account/EMI in a supported country; a Moroccan passport-holder director is commonly accepted [inference from vendor claims; Stripe's own onboarding rule for non-resident representatives not retrieved].
- UAE Stripe requires a UAE entity and UAE bank account; UAE bank onboarding for a non-resident owner without a visa is the known choke point [BK].

### Gaps
- PayPal Business availability per entity country and its treatment of non-resident owners: not researched (banking researcher's scope).
- Mercury, Relay, Wise Business, Airwallex, Revolut Business, Payoneer acceptance of Moroccan-resident UBOs: not researched. Anecdotally Mercury/Wise accept many non-US founders but run country-risk lists — unverified.
- Stripe's exact requirements for a US LLC with a foreign owner (EIN yes; SSN/ITIN not required; US address/phone expectations): not confirmed on docs.stripe.com.

## KQ8 — Ease of remote, mostly automated administration; service providers and prices

### Takeaway
Estonia is the only fully digital state stack (formation, signatures, filings via e-ID), the UK is close behind (online Companies House/HMRC, but ID verification and an accountant), and the US LLC is the lightest in obligations but has an archaic filing step (Form 5472 by fax/mail) with a $25,000 penalty for getting it wrong. UAE, Hong Kong and Singapore are agent-mediated rather than self-service.

### Cited Findings
- Stripe Atlas: $500 formation, $100/yr registered agent, includes EIN, 83(b) filing and templates, $2,500 Stripe credits — [stripe.com/atlas](https://stripe.com/atlas) [V]
- Form 5472 for foreign-owned DEs cannot be e-filed: fax 855-887-7737 or mail to IRS Ogden; extension by Form 7004 marked "Foreign-owned U.S. DE" — [IRS i5472](https://www.irs.gov/instructions/i5472) [V]
- BOI reporting no longer applies to US-formed entities (final rule effective 14 Aug 2026) — one fewer filing — [Morrison Foerster](https://www.mofo.com/resources/insights/260820-fincen-ends-beneficial-ownership-reporting) [V]
- Estonia: company registration online in 15 min–1 h for €265 — [e-resident.gov.ee](https://www.e-resident.gov.ee/start-a-company/) [V]
- Xolo Leap Pro ≈ €129/month (inferred from "two months free, up to €258"), 6-month minimum — [Xolo](https://www.xolo.io/zz-es/faq/xolo-leap/category/promotions/article/leap-pro-2-months-for-free---promotion) [S]
- UK: incorporation and confirmation statement filed digitally (£100 / £50); identity verification via GOV.UK One Login, Post Office or authorised agent — [GOV.UK fees](https://www.gov.uk/government/news/companies-house-fees-are-changing-from-1-february-2026); [GOV.UK ID verification](https://www.gov.uk/government/news/companies-house-confirms-identity-verification-rollout-from-18-november-2025) [V]
- UAE: corporate tax registration and annual return mandatory even at nil tax — [Gulf News](https://gulfnews.com/business/corporate-tax/uae-reminds-small-businesses-to-file-corporate-tax-returns-even-if-no-tax-is-due-1.500629117)
- UAE e-invoicing is being rolled out (referenced in 2026 regulatory round-ups) — [Entrepreneur ME "Two UAE Regulations SMEs Should Have on Their Radar"](https://mena.entrepreneur.com/?p=39715) [S, not opened]

### Inferences
- Automation ranking for a solo technical founder: (1) Estonia OÜ + Xolo/1Office/Companio-type provider (API-friendly banking, digital signatures, monthly declarations handled); (2) US LLC + annual 5472 preparer (one filing a year, but bookkeeping discipline needed to substantiate "reportable transactions"); (3) UK Ltd + online accountant (annual accounts, CT600, confirmation statement, possibly VAT); (4) UAE (annual licence renewal, CT return, possible audit, visa admin); (5) HK/SG (audit or resident officers).
- For a Moroccan passport-holder, UK online ID verification via the GOV.UK app may not support the document; using an authorised corporate service provider (ACSP) is the likely route — adds a small fee [inference; not verified].

### Gaps
- Current list prices for doola, Firstbase, Northwest/Wyoming agents, 1Office, Companio, Enty, Osome, Sleek: not retrieved — the comparison of providers is therefore incomplete.
- Estonia's monthly/annual filing set (TSD, annual report within 6 months, VAT threshold €40,000) is [BK], not verified.
- UK: whether a Moroccan passport works in the GOV.UK One Login ID-check app — not verified.

## KQ9 — Total cost of ownership (year 1 and steady state) and effective entity-level tax at 20k / 100k / 300k USD profit

### Takeaway
Fixed costs are a rounding error at 100k+ profit except in the UAE-with-visa, HK and Singapore; what differentiates structures is entity-level tax (0% conditional for US LLC and UAE-SBR, deferred for Estonia, 8–12% for HK/SG, 19–25% for UK, 21%+15% for a US C-corp) and, above all, how the founder's country of residence taxes him — which this note does not cover. At 20k profit only the US LLC, UK Ltd or Estonia OÜ are cost-proportionate.

### Cited Findings
- All rates and fees used are those cited in KQ2 and KQ3: [Stripe Atlas](https://stripe.com/atlas); [IRS i5472](https://www.irs.gov/instructions/i5472); [GOV.UK CT rates](https://www.gov.uk/government/publications/rates-and-allowances-corporation-tax/rates-and-allowances-corporation-tax); [GOV.UK Companies House fees](https://www.gov.uk/government/news/companies-house-fees-are-changing-from-1-february-2026); [KPMG Estonia 2026 tax card](https://assets.kpmg.com/content/dam/kpmgsites/ee/pdf/tax-cards/2026%20Tax%20Card-web.pdf.coredownload.inline.pdf); [e-resident.gov.ee](https://www.e-resident.gov.ee/start-a-company/); [Khaleej Times on SBR to 2029](https://www.khaleejtimes.com/business/uae-extends-corporate-tax-relief-for-small-businesses-until-2029); [Avyanco IFZA costs](https://avyanco.com/ifza-free-zone-cost/); [IRD HK two-tier](https://www.ird.gov.hk/eng/faq/2tr.htm); [IRAS rates](https://www.iras.gov.sg/irashome/Quick-Links/Tax-Rates/Corporate-Tax-Rates/); [PwC Morocco WHT](https://taxsummaries.pwc.com/morocco/corporate/withholding-taxes)

### Inferences
Researcher model (USD; fixed-cost ranges are estimates — government fees sourced, professional fees assumed; entity tax from the KQ3 table; excludes any tax in the founder's country of residence, payment-processor fees and VAT/sales tax):

| Structure | Year-1 fixed cost | Steady fixed cost/yr | Entity tax @20k | @100k | @300k | Fixed cost + entity tax as % of profit (steady) @20k / 100k / 300k |
|---|---|---|---|---|---|---|
| US LLC (WY/NM) | $300–1,000 | $300–900 | 0 | 0 | 0 | ≈ 1.5–4.5% / < 1% / < 0.3% |
| US LLC via Atlas (DE) | $500 + preparer ≈ $700–1,100 | $700–1,200 | 0 | 0 | 0 | ≈ 3.5–6% / ≈ 1% / < 0.5% |
| US C-Corp (DE, Atlas) | $500 + CPA ≈ $1,500–3,000 | $1,500–3,000 | 4,200 | 21,000 | 63,000 | ≈ 28–36% / ≈ 23–24% / ≈ 21.5–22% (before 15% dividend WHT) |
| UK Ltd | ≈ $1,000–2,500 | ≈ $1,000–2,600 | 3,800 | 21,600 | 74,600 | ≈ 24–32% / ≈ 23–24% / ≈ 25–26% |
| Estonia OÜ (retain) | ≈ $1,800–3,000 | ≈ $1,700–2,600 | 0 | 0 | 0 | ≈ 8.5–13% / ≈ 2–2.5% / < 1% (22% due on later distribution) |
| Estonia OÜ (distribute all) | same | same | 4,400 | 22,000 | 66,000 | ≈ 30–35% / ≈ 24–25% / ≈ 22.5–23% |
| UAE FZ, no visa, SBR | ≈ $4,000–6,000 | ≈ $4,000–6,000 | 0 | 0 | 0 | ≈ 20–30% / 4–6% / 1.3–2% |
| UAE FZ, 1 visa, SBR | ≈ $6,000–10,000 | ≈ $5,000–8,000 | 0 | 0 | 0 | ≈ 25–40% / 5–8% / 1.7–2.7% |
| UAE FZ, standard 9% (no SBR) | as above | as above | 0 | 0 | ≈ 17,800 | — / — / ≈ 7.5–8.5% |
| Hong Kong Ltd (onshore) | ≈ $3,000–6,000 (assumed) | ≈ $3,000–6,000 (assumed, incl. audit) | 1,650 | 8,250 | 28,400 | ≈ 23–38% / ≈ 11–14% / ≈ 10.5–11.5% |
| Singapore Pte Ltd (yrs 1–3) | ≈ $5,000–9,000 (assumed) | ≈ $5,000–9,000 (assumed, incl. resident director) | 850 | 5,200 | 34,700 | ≈ 29–49% / ≈ 10–14% / ≈ 13–14.5% |

- Reading the table: at 20k profit, anything other than a US LLC (or possibly a UK Ltd/Estonia OÜ on a cheap plan) burns a disproportionate share of profit in fixed cost; at 100k the US LLC, UAE-SBR and Estonia-retain models all sit at ≤ 6% entity-level burden; at 300k the UAE remains at ≤ 3% only while revenue stays ≤ AED 3m (SBR) — otherwise ≈ 8%.
- These numbers are *foreign-side only*. For a founder who remains tax-resident in Morocco, the US LLC's income is his income immediately; dividends from UK/Estonia/UAE/HK/SG companies are foreign-source dividends; and a company effectively managed from Morocco may itself be claimed as Moroccan-resident. The ranking can invert completely once Moroccan tax and exchange-control rules are applied — see the Moroccan-side research.
- Qualitative shortlist emerging from the foreign-side facts: (1) **US LLC (Wyoming or New Mexico; Delaware if via Atlas)** — cheapest, best Stripe/US-banking access, transparent; (2) **Estonia OÜ** — eligible for Moroccans, fully digital, EU credibility and OSS VAT, deferral, but no treaty with Morocco and card pickup abroad; (3) **UK Ltd** — treaty, credibility, simple, but 19–25% tax with no deferral; (4) **UAE free zone** — only compelling if combined with genuine relocation (visa + 90/183 days), then 0% (SBR to 2029) or 9%; (5) HK/Singapore/Ireland/Netherlands/Cyprus — over-engineered and costly for a solo founder; (6) Georgia — excluded (work must be done in Georgia; no Stripe); US C-corp — only if raising US venture capital.

### Gaps
- All professional-fee components (accounting, audit, nominee/resident director, registered office, 5472 preparation) in the TCO ranges are unsourced estimates; obtain live quotes before relying on them.
- FX rates used are assumptions (AED and HKD pegs are reliable; GBP, EUR, SGD rates were not looked up for Nov 2026).
- No sensitivity for VAT/sales-tax compliance cost, payment-processor/merchant-of-record fees (MoR typically ≈ 5% + fees), or currency-conversion costs when repatriating to Morocco.
- Interaction with Moroccan personal income tax on foreign dividends/business income, CFC-type or PoEM rules, and Office des Changes authorisations for a resident to hold foreign shares — out of scope here and decisive for the final ranking.
