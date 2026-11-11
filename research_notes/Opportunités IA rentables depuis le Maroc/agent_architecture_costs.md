# Agent architecture, capabilities, limits and costs for a centrally supervised multi-business AI system (as of 11 Nov 2026)

All pages were accessed on 2026-11-11 unless stated otherwise. Prices are USD list prices unless marked EUR. "Inferences" are my own arithmetic or judgement on top of the cited figures and are not sourced facts.

## 1. Anthropic API pricing, discounts, rate limits, server tools, subscription plans, and cheap alternatives

### Takeaway
The current Claude line-up spans an 80x input-price range ($0.10/MTok Haiku 5.5 to $8/MTok Fable 5.2), with a flat 50% Batch discount and cache reads at 2.5–10% of input price, so routing and caching dominate the bill far more than model list price. Subscriptions (Max $100, Ultra $200) are for an individual's interactive and scheduled use; a multi-business production system belongs on the API under the Commercial Terms, where a new account is capped at $500/month (Start tier) until it is promoted.

### Cited Findings

**Model prices (per million tokens, first-party API)**

| Model | Input | 5-min cache write | 1-h cache write | Cache read | Output | Batch in / out |
|---|---|---|---|---|---|---|
| Claude Fable 5.2 | $8 | $10 | $16 | $0.20 | $40 | $4 / $20 |
| Claude Fable 5.1 | $10 | $12.50 | $20 | $0.25 | $50 | $5 / $25 |
| Claude Opus 5.5 | $4 | $5 | $8 | $0.20 | $20 | $2 / $10 |
| Claude Opus 5 / 4.8 / 4.7 / 4.6 | $5 | $6.25 | $10 | $0.50 | $25 | $2.50 / $12.50 |
| Claude Sonnet 5.5 | $2 | $2.50 | $4 | $0.10 | $10 | $1 / $5 |
| Claude Sonnet 5 | $2 | $2.50 | $4 | $0.20 | $10 | $1 / $5 |
| Claude Sonnet 4.6 | $3 | $3.75 | $6 | $0.30 | $15 | $1.50 / $7.50 |
| Claude Haiku 5.5 (prompt ≤100K tokens) | $0.10 | $0.125 | $0.20 | $0.01 | $0.50 | $0.05 / $0.25 |
| Claude Haiku 5.5 (prompt >100K tokens) | $0.50 | $0.625 | $1 | $0.05 | $2.50 | $0.25 / $1.25 |
| Claude Haiku 4.5 | $1 | $1.25 | $2 | $0.10 | $5 | $0.50 / $2.50 |

— [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)

- Claude Mythos 5.2 / 5.1 carry the same prices as Fable 5.2 / 5.1 but are "limited availability" for verified organizations only, so they are not a planning option for a small operator. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Cache-read multipliers differ by model: 0.025x of input on Fable 5.2/5.1, 0.05x on Opus 5.5 and Sonnet 5.5, 0.1x on all other models. Cache writes cost 1.25x (5-minute) or 2x (1-hour). A 5-minute cache pays for itself after one read, a 1-hour cache after two. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Batch API: 50% off input and output, stackable with caching; results within 24 hours. Not combinable with fast mode, message threads or Managed Agents sessions. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing); [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Long context: Claude 4.6 and later (except Haiku 5.5) include the full 1M-token window at standard per-token prices. Haiku 5.5 is the exception: any request whose prompt exceeds 100,000 tokens is billed at 5x, output included. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Tokenizer: Claude 4.7 and later produce about 30% more tokens for the same text than Sonnet 4.6 and earlier, so per-token price comparisons with older models understate cost. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Fast mode (up to 2.5x output speed) doubles prices: Fable 5.2 $16/$80, Opus 5.5 $8/$40. US-only inference (`inference_geo: "us"`) adds a 1.1x multiplier. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)

**Server tools**
- Web search: $10 per 1,000 searches plus token cost of the results. Web fetch: no extra charge, tokens only (average 10 kB page ≈ 2,500 tokens; 100 kB documentation page ≈ 25,000 tokens; 500 kB research PDF ≈ 125,000 tokens). — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Code execution: free when used with the current web search / web fetch tools; otherwise 1,550 free container-hours per organization per month, then $0.05 per hour per container, 5-minute minimum. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Token overhead of tool definitions: tool-use system prompt ≈ 286 tokens on Opus 5.5 / Sonnet 5.5 / Haiku 5.5; bash tool +325; text editor +974; computer-use toolset ≈ 4,500; browser-use toolset ≈ 6,600 tokens per request, plus screenshots billed as image input. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)

**Rate limits and spend caps**
- Tiers are now named Start, Build, Scale, Custom (plus an "Evaluation" tier for new organizations with lower limits). Monthly spend caps: Start $500, Build $1,000, Scale $200,000. At the cap, API usage pauses until the first of the next month unless a tier increase is granted. — [Anthropic rate limits](https://platform.claude.com/docs/en/api/rate-limits)
- Start-tier limits: Fable 5.2 4,000 RPM / 500K ITPM / 100K OTPM; Opus 5.5, Sonnet 5.5 and Haiku 5.5 each 4,000 RPM / 2M ITPM / 400K OTPM. Build tier: Fable 5.2 10,000 RPM / 1.5M ITPM / 300K OTPM; the others 10,000 RPM / 5M ITPM / 1M OTPM. — [Anthropic rate limits](https://platform.claude.com/docs/en/api/rate-limits)
- Cache reads do not count toward ITPM. Batch queue: 200,000 requests in processing on Start, 100,000 per batch. — [Anthropic rate limits](https://platform.claude.com/docs/en/api/rate-limits)
- An organization can set its own lower monthly spend limit, and per-workspace spend and rate limits (not on the default workspace). — [Anthropic rate limits](https://platform.claude.com/docs/en/api/rate-limits)

**Subscription plans**
- Pro $20/month ($17 annual); "Max" (5x) $100/month; "Ultra" (20x) $200/month; Team standard seat $25 monthly / $20 annual; Team premium seat $125 / $100; Enterprise $20/seat with 20-seat minimum and usage billed at API rates. Claude Code is included from Pro upward. — [claude.com/pricing](https://claude.com/pricing)
- Max, Ultra and Team include monthly API credits: $100 (Max), $200 (Ultra), $20 per Team standard seat and $100 per premium seat, pooled and capped at $500. They cover the Claude API, Managed Agents, the Agent SDK and the playground; they do not cover Claude Code or extra usage in the apps; no rollover. Pro, Free and Enterprise are not eligible. When credits run out, requests stop unless purchased credits exist. — [API credits for subscribers](https://platform.claude.com/docs/en/about-claude/api-credits-for-subscribers)
- Agent SDK and `claude -p` signed in with a subscription "still draw from your subscription limits", including third-party app usage; a separate Agent SDK credit announced for 15 June 2026 was paused and replaced on 7 October 2026 by the monthly API credits above. — [Claude support: Agent SDK with your Claude plan](https://support.claude.com/en/articles/15036540-use-the-claude-agent-sdk-with-your-claude-plan)
- Consumer Terms (effective 8 Oct 2025) prohibit accessing the services "through automated or non-human means, whether through a bot, script, or otherwise" except via an Anthropic API key or where Anthropic explicitly permits it, and prohibit sharing account credentials. API keys and the Console fall under the Commercial Terms. — [Anthropic Consumer Terms](https://www.anthropic.com/legal/consumer-terms)
- Cloud scheduled tasks "belong to your individual claude.ai account", are not shared with teammates, and act through the owner's connected identities. — [Claude Code scheduled tasks](https://code.claude.com/docs/en/routines)

**Cheap alternatives for routing (per million tokens, input / cached input / output)**
- OpenAI: gpt-6-luna $0.10 / $0.01 / $0.50; gpt-5.6-luna $0.20 / $0.02 / $1.20; gpt-5-nano $0.05 / $0.005 / $0.40; gpt-6.1-terra $1 / $0.05 / $5; gpt-6.1-sol $2 / $0.10 / $10; gpt-6-astra $10 / $1 / $50. Batch and Flex are about half price. Web search tool $10 per 1,000 calls. — [OpenAI API pricing](https://developers.openai.com/api/docs/pricing)
- Google Gemini: 3.1 Flash-Lite $0.25 / $1.50; 3.5 Flash-Lite $0.30 / $2.50; 3.8 Flash $0.75 / $3.75 until 31 Dec 2026, then $1.50 / $7.50; Gemini 4 Carbon and Argon $2 / $10 until 30 Nov 2026, then $4 / $20. Batch about 50% lower. Search grounding: 5,000 free requests/month, then $14 per 1,000. Free tier exists for Flash models but content may be used to improve Google products. — [Gemini API pricing](https://aistudio.google.com/docs/pricing)
- DeepSeek (open-weight family, first-party API): deepseek-flash $0.30 in / $1.20 out peak and $0.15 / $0.60 off-peak (cache hit $0.006 / $0.003); deepseek-v4-pro $1.32 / $3.96 peak, $0.66 / $1.98 off-peak. — [DeepSeek pricing](https://api-docs.deepseek.com/quick_start/pricing)

### Inferences
- Haiku 5.5 at $0.10/$0.50 matches OpenAI's cheapest current-generation tier (gpt-6-luna) and undercuts Gemini Flash-Lite and DeepSeek-flash peak rates, so the cost argument for multi-vendor routing is weak in November 2026; the remaining reasons to add a second vendor are resilience and independent verification, not price.
- A realistic production path is: one API organization under the Commercial Terms, one workspace per business with its own spend limit, plus optionally one Max or Ultra seat for the human operator (interactive Claude Code, with $100–200 of API credit as a bonus). Running several businesses' unattended automation through a personal subscription conflicts with the plan's individual-account design and the consumer-terms automation clause except where Anthropic explicitly allows it (Claude Code headless, Agent SDK, scheduled tasks).
- The $500 Start cap and $1,000 Build cap are binding constraints for a "heavy" scenario; plan a tier-increase request before scaling.
- Gemini 4 and Flash prices double on 1 Dec 2026 and 1 Jan 2027, so any budget using Gemini must use the post-promotion prices.

### Gaps
- OpenRouter per-model prices for open-weight models (Qwen, Llama, Mistral, Kimi, GLM) could not be extracted; only DeepSeek's first-party prices were verified.
- The Consumer Terms page does not mention Max or Ultra by name; which terms govern those plans was not verified. The Commercial Terms text was not fetched.
- Deposit thresholds for moving between Start, Build and Scale are no longer shown on the rate-limit page (promotion is described as automatic, based on usage history).
- Weekly/5-hour usage allowances of Pro/Max/Ultra in tokens are not published.

## 2. Claude Code, Agent SDK, Managed Agents, multi-agent features, MCP, memory, computer use: what is production-ready, and measured reliability limits of autonomous agents

### Takeaway
The hosted agent stack exists but most of it is still labelled beta or research preview in November 2026: Managed Agents is beta, cloud scheduled tasks are research preview, agent teams are experimental. Independent evidence (METR, Vending-Bench 2, Project Vend) shows agents can sustain multi-hour technical tasks and turn a profit in simulation, yet remain exploitable by social manipulation, over-generous with refunds, and far below a competent human baseline on a year-long business task.

### Cited Findings

**Building blocks and status**
- Claude Code headless: `claude -p` runs non-interactively with `--allowedTools`, `--permission-mode`, `--output-format json|stream-json`, `--json-schema`, `--max-budget-usd`, session resume, and returns `total_cost_usd`. `--bare` mode (recommended for scripts, future default) requires `ANTHROPIC_API_KEY` and does not use subscription login. `--permission-prompts none` denies anything that would need a human. — [Claude Code headless docs](https://code.claude.com/docs/en/headless)
- Claude Agent SDK: the same agent loop, tools and context management as Claude Code, as CLI, Python and TypeScript packages; you host it yourself. — [Claude Code headless docs](https://code.claude.com/docs/en/headless)
- Cloud scheduled tasks (formerly "routines"): research preview; triggers are schedule, API (HTTP POST with bearer token, beta header `experimental-cc-routine-2026-04-01`), and GitHub events; cron intervals shorter than one hour are rejected; 100 scheduled runs per hour per account; runs draw down subscription usage; available on Pro, Max, Ultra, Team, Enterprise; runs start in "auto mode" where a classifier approves or blocks actions. — [Claude Code scheduled tasks](https://code.claude.com/docs/en/routines)
- Claude Managed Agents: beta (header `managed-agents-2026-04-01`), enabled by default for all API accounts; Anthropic runs the agent loop and a per-session sandbox (bash, file operations, web search/fetch, MCP servers); supports scheduled deployments on cron; self-hosted sandboxes possible. Not eligible for Zero Data Retention or HIPAA BAA. MCP tunnels and "dreaming" are a more limited research preview. Rate limits: 300 create requests/minute, 1,200 reads/minute. — [Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview); [rate limits](https://platform.claude.com/docs/en/api/rate-limits)
- Managed Agents pricing: standard token rates plus $0.08 per session-hour, metered only while status is `running` (idle time is free); no Batch discount; web search at the usual $10/1,000. Anthropic's worked example: a 1-hour Opus 5.5 session with 50K input and 15K output tokens costs $0.58, or $0.428 with 40K tokens read from cache. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Managed Agents session budgets: a dollar cap per session; the session pauses with `stop_reason: budget_reached`. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Agent teams in Claude Code are disabled by default and enabled with `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`; they use about 7x the tokens of a standard session when teammates run in plan mode. — [Claude Code costs](https://code.claude.com/docs/en/costs)
- Computer use and browser use are offered as API toolsets (`computer_toolset_20260801`, `browser_toolset_20260801`) with roughly 4,500 and 6,600 tokens of definition overhead per request. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)

**Reliability evidence**
- METR: Claude Mythos Preview was added on 8 May 2026 as the last Claude entry; the time-horizons page states it "is no longer actively updated" (8 Sept 2026) and that "measurements above 16 hrs are unreliable with our current task suite". Tasks are mainly software engineering, ML and cybersecurity, self-contained and automatically scored; METR says real-world work is messier. No Fable or Opus 5 measurement is published. — [METR time horizons](https://metr.org/time-horizons/)
- Secondary reports put Mythos Preview's 50% time horizon at about 16–17 hours (95% CI 8.5–55 hours) and Opus 4.6 at roughly 12–14.5 hours at 50% but only about 1 h 10 min at 80% success. — [OfficeChai](https://officechai.com/ai/exponential-progress-claude-opus-4-6-has-50-time-horizon-of-14-5-hours-on-metr-time-horizons-benchmark); [LessWrong reanalysis](https://www.lesswrong.com/posts/kNHxuusznCR3rhqkf/is-metr-underestimating-llm-time-horizons); [METR limitations note](https://metr.org/notes/2026-01-22-time-horizon-limitations/)
- Vending-Bench 2 (Andon Labs; simulated year running a vending business from $500): current leaderboard top is Gemini 4 Carbon $16,484, GPT-6 Astra $15,515, GPT-6 Sol $14,428; Claude Opus 5 $11,182, Claude Sonnet 5.5 $11,165, Claude Opus 4.7 $10,937. Andon Labs estimates a "good" strategy would earn about $63K in the year, so the best models reach roughly a quarter of that. Stressors include adversarial suppliers, bait-and-switch pricing, delayed deliveries and refund demands. — [Andon Labs Vending-Bench 2](https://andonlabs.com/evals/vending-bench-2)
- Project Vend phase two (Anthropic and Andon Labs, real shop, Sonnet 4 then 4.5): weeks with negative margin were largely eliminated after adding a CRM, cost-aware inventory records, price/delivery verification procedures and payment links; Anthropic's takeaway is that "bureaucracy matters". Still observed: readiness to sign a contract that conflicted with a US law, an offer of $10/hour (below California minimum wage), staff convincing the agent that someone else had been elected CEO, refunds tripling and store credits doubling, a same-model "CEO" agent that approved lenient requests about eight times as often as it denied them, and unproductive agent-to-agent chat loops. Conclusion: the gap between "capable" and "completely robust" remains wide and the agents needed substantial human support. — [Anthropic Project Vend 2](https://www.anthropic.com/research/project-vend-2)
- Anthropic on production agents: "Agents are stateful and errors compound"; "minor issues for traditional software can derail agents entirely". — [Anthropic multi-agent research system](https://www.anthropic.com/engineering/multi-agent-research-system)
- Anthropic's own task-level pass rates show the residual failure rate on well-specified work: Haiku 5.5 passed 93% of a 79-task Managed Agents set at about $0.011 per passed attempt; Opus 5.5 solved 92.8% of a SWE-bench Pro subset at medium effort; Fable 5.2 scored 54.5–57.7% on DeepResearch Bench II. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)

### Inferences
- A supervisor of the same model family shares the workers' blind spots (Project Vend's CEO result), so a "Fable supervises Haiku" hierarchy adds capability but not independent judgement on commercial leniency or manipulation; hard rules in code (refund ceilings, price floors, contract templates) are what fixed Vend's margins.
- A 5–8% failure rate per well-specified task compounds quickly across chained steps, which argues for short, checkable tasks with deterministic validation between them rather than long unattended sessions.
- For an operator who wants minimum infrastructure, Managed Agents scheduled deployments are the closest thing to a hosted "agent cron"; the runtime fee is negligible (100 session-hours a month is $8) next to tokens. The trade-off is beta status and no batch discount.
- Claude Code cloud scheduled tasks suit an owner's personal automations (hourly at most) but not a multi-tenant production backend, given research-preview status, one-hour minimum interval and individual-account scope.

### Gaps
- MCP connector status, memory tool and memory stores, compaction and context-editing betas were not verified on live pages in this session. Claude Code's bundled API reference (cached 2026-11-03) lists: memory tool `memory_20250818` (no beta header), Managed Agents memory stores (beta `agent-memory-2026-07-22`), MCP connector (beta `mcp-client-2025-11-20`), compaction (beta `compact-2026-01-12`), context editing (beta `context-management-2025-06-27`), Files API and Skills out of beta. Treat as probable, not live-verified; see [features overview](https://platform.claude.com/docs/en/build-with-claude/overview).
- No METR measurement exists for Fable 5.x, Opus 5.x or Sonnet 5.5; the numeric Mythos/Opus 4.6 horizons come from secondary sources.
- Vending-Bench 2 lists 74 models but only the top 10 were retrieved; Fable 5.2 and Opus 5.5 positions are unknown.
- No independent, peer-reviewed failure-rate study of agents running real online businesses in 2026 was found beyond Project Vend.

## 3. Orchestrators: n8n, LangGraph/LangSmith, Temporal, Inngest, Trigger.dev, Make, Zapier, and when cron + queue + DB suffices

### Takeaway
Hosted orchestration costs between $0 and about $100 a month at micro-business volumes, so the choice should be driven by licence and durability needs rather than price. n8n's Sustainable Use License permits internal business use but restricts providing the software to others commercially, which matters if the "operating system" is ever sold as a service.

### Cited Findings
- n8n Cloud (annual billing): Starter €20/month for 2,500 executions, 5 concurrent, 5-minute maximum execution; Pro €50/month for 10,000 executions, 40-minute maximum; Business €667/month for 40,000 executions, self-hosted only; Enterprise custom. Without a licence key, self-hosted n8n runs as the free Community edition. — [n8n pricing](https://n8n.io/pricing/); [n8n hosting docs](https://docs.n8n.io/hosting/)
- n8n Sustainable Use License: "You may use or modify the software only for your own internal business purposes or for non-commercial or personal use"; "You may distribute the software or provide it to others only if you do so free of charge for non-commercial purposes." — [n8n LICENSE.md](https://raw.githubusercontent.com/n8n-io/n8n/master/LICENSE.md)
- LangSmith: Developer $0 with 5,000 base traces/month and one seat; Plus $39/seat/month with 10,000 base traces; base traces retained 14 days, extended 180 days. Deployments metered at $0.0675 per vCPU-hour and $0.009 per GiB-hour for runtime, $0.177 per vCPU-hour and $0.025 per GiB-hour for the database. — [LangChain pricing](https://www.langchain.com/pricing)
- Temporal Cloud: pay-as-you-go from $50 per million actions with no base fee (falling to $25 at volume), $0.042 per GB-hour active storage; Business support add-on from $500/month; $150 credit for 90 days for new sign-ups. — [Temporal pricing](https://temporal.io/pricing)
- Inngest: Free 50,000 executions/month and 5 concurrent steps (execution pauses at quota); Pro from $99/month for 1M executions and 100 concurrent steps, then $50 per additional million; each step counts as an execution. — [Inngest pricing](https://www.inngest.com/pricing)
- Trigger.dev: Free with $5 usage, 20 concurrent runs, 10 schedules; Hobby $10/month with $10 usage, 50 concurrent runs, 100 schedules; Pro $50/month, 200+ concurrent, 1,000+ schedules. Compute $0.0000338/second on the default 0.5 vCPU machine plus $0.000025 per run. — [Trigger.dev pricing](https://trigger.dev/pricing)
- Zapier: Free 100 tasks/month; Professional $19.99/month annual for 750 tasks, $49 for 2,000 tasks, $129 for 10,000 tasks; Team $69 for 2,000 and $169 for 10,000 tasks (annual). — [Zapier pricing](https://zapier.com/pricing)
- Make: Free plan 1,000 credits/month; most actions consume 1 credit, AI features via Make's AI provider may use more. — [Make pricing](https://www.make.com/en/pricing)
- Cloudflare offers a serverless equivalent of "cron + queue + DB": Workers Paid $5/month with 10M requests; Queues 1M operations/month included then $0.40 per million; D1 with 25B row reads and 50M row writes included; Workflows with 500K steps/month included then $0.80 per 100K. — [Cloudflare Workers pricing](https://developers.cloudflare.com/workers/platform/pricing/)

### Inferences
- A Zapier workflow that fires on 5,000 tender notices a day would consume about 150,000 tasks a month, far beyond the $169 tier; per-task SaaS automation is unsuitable for high-volume classification and should be reserved for low-volume glue.
- For a single operator running several internal businesses, self-hosted n8n Community edition is licence-compatible (internal business purposes). Reselling hosted n8n workflows to clients or embedding n8n in a paid product is the case the licence restricts and would need n8n's commercial agreement.
- Cron + a Postgres table used as a queue + idempotent workers is sufficient when jobs are short (under a few minutes), retries are simple, and there are fewer than roughly a dozen workflow types. A durable-execution engine (Temporal, Inngest, Trigger.dev, Cloudflare Workflows) earns its place once workflows wait hours or days for human approval, need resumable multi-step state, or must fan out with concurrency limits. This is a design judgement, not a sourced threshold.
- Trigger.dev Hobby ($10) or Inngest Free cover the light scenario; a 10-minute agent job on Trigger.dev's default machine costs about $0.02 in compute, negligible next to model tokens.

### Gaps
- n8n's documentation page with worked allowed/not-allowed examples of the Sustainable Use License returned "page not found"; only the licence text itself was verified.
- Make's paid plan prices (Core, Pro, Teams) were not present in the fetched page.
- LangSmith's per-trace overage price and LangGraph per-node pricing are not shown on the pricing page.
- Temporal's self-hosted open-source option is not mentioned on its pricing page and was not separately verified.

## 4. Infrastructure costs: VPS, serverless, email, observability, browser automation, payments, helpdesk, scraping legality

### Takeaway
Core infrastructure for several micro-businesses fits in roughly $30–150 a month; the notable 2026 change is that Hetzner raised cloud prices twice and its cheapest lines are reported unavailable for new orders. Merchant-of-record billing costs 5% + $0.50 per transaction at both Paddle and Lemon Squeezy, which is material on low-priced products.

### Cited Findings
- Hetzner Cloud now lists Cost-Optimized (shared) from €5.99/month, Regular Performance (shared) from €5.49/month, and General Purpose (dedicated vCPU) from €36.99/month, excluding VAT. — [Hetzner Cloud](https://www.hetzner.com/cloud/)
- Hetzner's price adjustment of 15 June 2026 applies to new orders and rescales; existing servers are not repriced. — [Hetzner price adjustment notice](https://docs.hetzner.com/general/infrastructure-and-availability/price-adjustment/)
- Secondary sources report CX23 rising from €3.99 to €5.49 and CAX11 from €4.49 to €5.99, CPX22 rising to €19.49, an earlier increase from 1 April 2026 attributed to DRAM and NAND costs, and all Cost-Optimized plans showing a disabled order button in September–October 2026. — [Northflank](https://northflank.com/blog/hetzner-cloud-server-price-increases); [Bitdoze](https://www.bitdoze.com/hetzner-cloud-cost-optimized-plans/); [WZ-IT](https://wz-it.com/en/blog/hetzner-price-increase-june-2026-cpx-ccx-alternatives/)
- DigitalOcean basic droplets: 1 GiB/1 vCPU $6; 2 GiB/1 vCPU $12; 4 GiB/2 vCPU $24; 8 GiB/4 vCPU $48 per month. — [DigitalOcean droplet pricing](https://www.digitalocean.com/pricing/droplets)
- Supabase: Free with 500 MB database and 50,000 MAU, projects paused after one week of inactivity; Pro from $25/month with 8 GB database per project, 100,000 MAU, 250 GB egress and $10 compute credit. — [Supabase pricing](https://supabase.com/pricing)
- Neon Postgres: Free 100 CU-hours per project and scale-to-zero after 5 minutes; Launch $0.106 per CU-hour and $0.35 per GB-month. — [Neon pricing](https://neon.com/pricing)
- Cloudflare Workers Paid: $5/month minimum, 10M requests and 30M CPU-ms included; R2 storage $0.015/GB-month with free egress. — [Cloudflare Workers pricing](https://developers.cloudflare.com/workers/platform/pricing/)
- Email: Resend Free 3,000 emails/month (100/day, 3 domains), Pro $20 for 50,000 emails and 10 domains. Postmark Basic $15 for 10,000 emails then $1.80 per 1,000; inbound processing on Pro ($16.50) and above. Amazon SES $0.10 per 1,000 outbound and $0.10 per 1,000 inbound emails, dedicated IP $24.95/month. — [Resend pricing](https://resend.com/pricing); [Postmark pricing](https://postmarkapp.com/pricing); [Amazon SES pricing](https://aws.amazon.com/ses/pricing/)
- Observability: Langfuse Hobby free with 50,000 units/month and 30-day data access; Core $29/month with 100,000 units then $8 per 100,000; Pro $199/month; open source and free to self-host. — [Langfuse pricing](https://langfuse.com/pricing)
- Browser automation: Browserbase Developer $20/month with 100 browser-hours, 25 concurrent sessions and 1 GB proxy, overage $0.12 per browser-hour and $12 per GB proxy; Startup $99/month with 500 hours and 5 GB. — [Browserbase pricing](https://www.browserbase.com/pricing)
- Payments: Paddle charges 5% + $0.50 per checkout transaction as merchant of record, covering sales tax/VAT filing, fraud and chargeback handling; products priced under $10 require bespoke pricing. Lemon Squeezy charges 5% + $0.50 per sale, with possible small additional fees on international and edge-case payments, payouts twice a month. — [Paddle pricing](https://www.paddle.com/pricing); [Lemon Squeezy pricing](https://www.lemonsqueezy.com/pricing)
- Scraping and platform rules: Anthropic's Usage Policy prohibits using Claude to circumvent the guardrails or terms of other platforms, and prohibits automated account creation. — [Anthropic Usage Policy](https://www.anthropic.com/legal/aup)

### Inferences
- On a $9 product, 5% + $0.50 is $0.95, about 10.6% of revenue; on a $49 product it is $2.95, about 6%. Micro-priced products should be bundled or priced above roughly $20 to keep MoR fees under 8%.
- A baseline stack of one 4–8 GB VPS (€6–20 or $24–48), Supabase Pro ($25) or self-hosted Postgres, Resend free or Pro ($0–20), Langfuse self-hosted or Core ($0–29), and Cloudflare Workers ($5) lands at roughly $35–125 a month before browser automation.
- Browser sessions are cheap relative to the tokens they generate: one browser-hour is $0.12, while a computer-use loop sending screenshots plus a 6,600-token toolset definition on every turn can cost dollars per hour in tokens. Prefer APIs and HTTP fetch over browser driving wherever a site offers them.
- Scraping that requires logging in, bypassing anti-bot measures or violating a site's terms is exposed both to the target site's legal claims and to Anthropic's policy clause on circumventing other platforms' terms; public-data collection through official APIs, feeds and open-data portals (for example public tender portals) is the low-risk design.

### Gaps
- OVH, Vercel, Helicone, Sentry and Grafana Cloud pricing were not retrieved in this session.
- Exact current Hetzner per-plan specifications and prices come from secondary sources; the official page shows only "from" prices by category.
- No authoritative 2026 legal source on web-scraping law (EU, US, Morocco) was retrieved; the legality points above are limited to Anthropic's policy text.
- Whether Paddle or Lemon Squeezy onboard Morocco-resident sellers, and payout options to Moroccan banks, was not checked.
- Helpdesk tooling pricing (for example Zendesk, Intercom, Crisp, Chatwoot) was not researched.

## 5. Cost-optimization patterns with quantified savings, verification, guardrails and security

### Takeaway
Anthropic's own measurements put caching at a 3–7x cost reduction on agent loops, batch at a flat 50%, and effort or model down-routing at 2–10x, while multi-agent fan-out multiplies token use roughly 4–15x versus chat. Prompt injection remains a measurable, non-zero risk for any agent that reads customer email or web pages, so least privilege and approval gates are structural requirements rather than optional hardening.

### Cited Findings

**Caching, batch, context**
- Without caching, cost was 3.3x (Opus 5.5) and 3.1x (Sonnet 5.5) on SWE-bench Pro, 1.7x on short Managed Agents sessions with Haiku 5.5, and 7.3x on a Sonnet 5.5 triage agent. On DeepResearch Bench II, Fable 5.1 cost $40.58 per task without caching versus $5.64 with it; Sonnet 5.5 $5.13 versus $1.05. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Healthy agent loops read a median 84% of input from cache (top decile 94%+); below about 80% suggests a cache-breaking change. Editing the system prompt mid-conversation on a ~100K-token conversation costs up to $1.26, about 25–50x the same text sent as a mid-conversation system message. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Tool search with a 502-tool catalogue cut a run from $1.02 to $0.56; programmatic tool calling used 24% fewer input tokens on agentic search; uploading a 1,862-row CSV to code execution instead of pasting it gave 25/25 correct for $0.40 versus 7/25 correct for $5.01; compaction saved 32% and pruning 39% on long runs, while context editing added 73% on a short run. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Output length is a direct lever: a one-line answer cost $0.49 per run versus $1.40 for a six-section memo at similar accuracy (78–85%). — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)

**Model and effort routing**
- SWE-bench Pro subset, cost per solved task: Sonnet 5.5 (high) 87.6% at $0.11; Opus 5.5 (low) 87.4% at $0.12; Opus 5.5 (medium) 92.8% at $0.22; Fable 5.1 (high) 92.3% at $1.19. Fable 5.2 on 463 problems: 96.3% at $1.39 (high), 94.6% at $0.39 (low); Opus 5.5 at xhigh 96.5% at $0.75. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Deep research (DeepResearch Bench II, 44 tasks): Fable 5.2 cost 4.3x Sonnet 5.5 "for no measurable gain" and 2.9x Opus 5.5 for a score 1.9 points lower; Fable 5.2 per task $1.49 (low), $2.16 (medium), $4.82 (high). — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Haiku 5.5 reached 85% on GPQA Diamond versus 91% for Opus 5.5 and Sonnet 5.5, at about 1/20 of Opus 5.5's and 1/10 of Sonnet 5.5's cost per correct answer. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Escalate-on-failure: running Opus 5.5 at low effort and re-running failures at high solved about 97% at about $0.17 per task, versus 95.3% at $0.29 for everything at high (about 40% cheaper); it requires a reliable failure signal such as tests or a verifier. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)

**Multi-agent overhead and supervisor patterns**
- "Agents typically use about 4× more tokens than chat interactions, and multi-agent systems use about 15× more tokens than chats"; token usage alone explained 80% of performance variance on BrowseComp; the multi-agent system beat single-agent Opus 4 by 90.2% on Anthropic's internal research eval; domains where agents must share context are "not a good fit for multi-agent systems today". — [Anthropic multi-agent research system](https://www.anthropic.com/engineering/multi-agent-research-system)
- Orchestrator results: Opus 5.5 orchestrating Sonnet 5.5 sub-agents cost about a third less than Opus 5.5 alone at about the same score; swapping in Fable 5.2 as orchestrator cost 19% more for about the same score; Haiku 5.5 sub-agents under Opus 5.5 cut cost per attempt 32% with a pass rate about 4 points lower. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Advisor pattern: Opus 5.5 with a Fable 5.1 advisor gained 1.7 points (edge of noise) for about 2.1x cost; Haiku 5.5 with an Opus 5.5 advisor cost 12% more on GPQA with no measurable gain. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Claude Code agent teams: about 7x tokens of a standard session. Average Claude Code cost across enterprise deployments is about $13 per developer per active day, $150–250 per month, under $30 per active day for 90% of users. — [Claude Code costs](https://code.claude.com/docs/en/costs)

**Guardrails and security**
- Spend controls available natively: organization and workspace monthly spend limits; `--max-budget-usd` per headless Claude Code run; Managed Agents per-session dollar budgets; `max_tokens` does not make the model economize (capped turns are discarded and still billed). — [Anthropic rate limits](https://platform.claude.com/docs/en/api/rate-limits); [Claude Code headless docs](https://code.claude.com/docs/en/headless); [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Headless runs without `--bare` execute a project's hooks and connect its MCP servers even in an untrusted folder, with no trust dialog. — [Claude Code headless docs](https://code.claude.com/docs/en/headless)
- Cloud scheduled tasks include all connected connectors by default, and Claude "can use an included connector during a run, including writes"; Anthropic advises removing those the task does not need. — [Claude Code scheduled tasks](https://code.claude.com/docs/en/routines)
- Prompt injection, as reported from Anthropic system cards by the press: for Claude Opus 4.8, browser-agent attack success was 31.5% without safeguards and 0.5% with safeguards across 129 environments (Gray Swan adaptive attacker); for Claude Opus 5, 3.7% without extra defences and 0% with auto mode, and on Gray Swan's indirect-injection benchmark 2.0% success within 15 attempts (0.2% single attempt). — [VentureBeat](https://venturebeat.com/security/anthropic-browser-agent-hijacked-31-percent-before-safeguards-engaged); [Xenospectrum](https://xenospectrum.com/en/claude-opus-5-prompt-injection/); [Cybersecurity News](https://cybersecuritynews.com/claude-opus-5-reduces-prompt-injection-attack/)
- Managed Agents is not eligible for Zero Data Retention; session transcripts persist until deleted. — [Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview)

### Inferences
- Anthropic's data argues against using Fable 5.2 as a routine orchestrator: it cost 19% more than Opus 5.5 in that role for the same score, and 3–4x more on deep research without a gain. A defensible allocation is Haiku 5.5 for classification and extraction, Sonnet 5.5 for drafting and tool-using workers, Opus 5.5 for orchestration, and Fable 5.2 reserved for a small number of weekly strategy and review calls where its ceiling matters, ideally at low or medium effort.
- Prompt caching's 5-minute lifetime means low-traffic workloads (a few emails an hour) get little benefit; for those, the Batch API's flat 50% is the dependable discount. The two stack for bursty batch jobs with a shared prefix.
- A 0.2–2% injection success rate per attempt is not negligible for an inbox that receives thousands of untrusted messages: assume occasional success and limit blast radius. Practical design: the agent that reads untrusted content has no send-money, delete or credential-bearing tools; outbound email, refunds above a threshold, price changes and contract acceptance go through an approval queue; secrets live in a vault or environment substitution outside the model's context; each business gets its own API workspace, keys and spend limit; a global kill switch disables schedulers and revokes keys.
- Independent verification is cheapest when it is deterministic (schema validation, totals reconciling, link checks, tests). A second-model check with a different vendor is the next step; a same-model reviewer is weakest (Project Vend CEO result).
- Per-task budget caps should be set in dollars at the orchestration layer (session budget or `--max-budget-usd`), not via `max_tokens`.

### Gaps
- The prompt-injection figures were not verified against Anthropic's system cards directly, and no published figure for Fable 5.2, Opus 5.5, Sonnet 5.5 or Haiku 5.5 was found.
- The second half of Anthropic's cost-optimization page (about 117K characters) was not read.
- No quantified study of secrets leakage or least-privilege effectiveness for agent deployments was retrieved.

## 6. Human-in-the-loop requirements and Anthropic usage-policy constraints

### Takeaway
Anthropic's Usage Policy (version effective 12 Nov 2026) makes the deployer responsible for everything an agent does through its tools, bans spam and AI-as-human deception, and requires qualified human review plus disclosure for individual decisions in legal, medical, financial, credit, insurance, housing, employment and education areas. Evidence from Project Vend indicates that disputes, negotiation under pressure and legal judgement still need a person.

### Cited Findings
- Agentic use must comply with the Usage Policy; users are "responsible for ensuring that agents they build or deploy" comply, including actions taken through tools, browsers or connected systems. — [Anthropic Usage Policy](https://www.anthropic.com/legal/aup)
- Spam: the policy bars promoting or facilitating "the generation or distribution of spam", and bars automation in account creation and creating multiple accounts to evade detection. — [Anthropic Usage Policy](https://www.anthropic.com/legal/aup)
- Disclosure: consumer-facing chatbots or agents that communicate directly with external users must disclose that they are AI, at minimum at the start of each session or in the product interface; attempting to "convince people they are interacting with a human when they are not" is prohibited. — [Anthropic Usage Policy](https://www.anthropic.com/legal/aup)
- High-risk recommendations: in legal, medical (including mental health), finance (personalized investment recommendations, individual tax advice), credit, insurance, housing, employment, education/credentials, healthcare access and public benefits, a qualified person must meaningfully review the recommendation with authority to change it before it is delivered or used, and the affected individual must be told AI was used. Wholly favourable decisions (for example paying a claim in full) are exempt where the law permits; internal drafting, research and business operations that do not decide about a specific individual are excluded. — [Anthropic Usage Policy](https://www.anthropic.com/legal/aup)
- Fake reviews, sockpuppets and astroturfing are prohibited, as is building or marketing tools for them; circumventing other platforms' guardrails or terms is prohibited; training models on outputs without authorization is prohibited. — [Anthropic Usage Policy](https://www.anthropic.com/legal/aup)
- Observed agent failures requiring human rescue in a real business: missing a legal conflict in a contract, proposing sub-minimum-wage pay, accepting a false claim about who was in charge, excessive refunds and credits, and needing humans "for getting out of customer disputes" and all physical tasks. — [Anthropic Project Vend 2](https://www.anthropic.com/research/project-vend-2)
- Unattended runs are designed to stop rather than guess when approval is needed: with `--permission-prompts none`, anything that would prompt is denied; in cloud scheduled tasks, repeated classifier blocks surface a permission prompt that "waits until someone answers it". — [Claude Code headless docs](https://code.claude.com/docs/en/headless); [Claude Code scheduled tasks](https://code.claude.com/docs/en/routines)
- Subscription accounts cannot be shared and consumer services cannot be accessed by bots or scripts outside Anthropic-permitted routes. — [Anthropic Consumer Terms](https://www.anthropic.com/legal/consumer-terms)

### Inferences
- Tasks that should stay human-owned in late 2026, combining the policy text with the Vend evidence: company formation, KYC/identity verification and bank or payment-provider onboarding (identity-bound and anti-automation by design); signing contracts and accepting terms; moving money, payouts and refunds above a small ceiling; chargeback and dispute responses; tax filings; live sales or negotiation calls; any decision about a named individual in a high-risk area; first-contact cold outreach at volume (spam exposure under both Anthropic policy and email/privacy law).
- Cold-email "AI SDR" businesses are the highest policy-risk model in this set: volume outreach sits next to the spam prohibition, and agents must not pose as humans. Opt-in, low-volume, clearly AI-disclosed outreach is the defensible form.
- A realistic steady-state human load for several micro-businesses is a daily approval-queue review plus weekly finance and strategy review, rather than zero; this is a planning judgement, not a measured figure.

### Gaps
- No sourced 2026 data was found on agent success rates for sales calls, KYC flows, bank operations or dispute handling specifically; the list above is inferred.
- The Usage Policy text was read through a summarizer; exact clause wording for high-risk areas should be checked against the page before legal reliance. The version fetched states an effective date of 12 Nov 2026, one day after access.
- Email-law constraints (CAN-SPAM, GDPR/ePrivacy, Moroccan Law 09-08) were not researched.

## 7. Worked cost examples and monthly budget scenarios

### Takeaway
At November 2026 list prices the four reference workloads cost roughly $1–5 per weekly briefing, $1–50 per 1,000 ten-page documents depending on model, $1–15 per 500 support emails, and about $85–170 a month for screening 5,000 tender notices a day with a Haiku-then-Sonnet cascade. Total AI plus infrastructure lands near $70–200 a month for a light portfolio, $500–1,200 for medium and $3,000–8,000 for heavy, with the heavy case exceeding the default API spend caps.

### Cited Findings
- Unit prices used below: Haiku 5.5 $0.10/$0.50 (batch $0.05/$0.25); Sonnet 5.5 $2/$10 (batch $1/$5, cache read $0.10); Opus 5.5 $4/$20 (batch $2/$10); Fable 5.2 $8/$40 (batch $4/$20, cache read $0.20); web search $0.01 per search. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Anthropic-measured anchors: a deep-research task costs $1.05 on Sonnet 5.5 with caching and $1.49–$4.82 on Fable 5.2 depending on effort; a short Managed Agents task on Haiku 5.5 costs about $0.011 per passed attempt; an agentic coding attempt costs $0.84 on Opus 5.5 and $1.34 on Fable 5.2. — [Anthropic cost-optimization docs](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)
- Web page token sizes: about 2,500 tokens for an average 10 kB page, 25,000 for a large page. — [Anthropic pricing docs](https://platform.claude.com/docs/en/about-claude/pricing)
- Spend caps: Start $500/month, Build $1,000/month, Scale $200,000/month. — [Anthropic rate limits](https://platform.claude.com/docs/en/api/rate-limits)

### Inferences

All figures in this section are my calculations from the cited unit prices. Token volumes are assumptions, stated for each case; thinking tokens are billed as output and can raise output volume above the figures assumed.

**A. Weekly intelligence briefing from 20 sources**
- Assumptions: 20 sources averaging 8,000 tokens each (160K tokens), 20 web searches.
- Pipeline design: Haiku 5.5 summarizes each source (160K in, 12K out) = $0.02; Fable 5.2 writes the synthesis from the summaries (20K in, 10K out including thinking) = $0.16 + $0.40 = $0.56; searches $0.20. Total about $0.80 per briefing, about $3.50 a month.
- Same pipeline with Opus 5.5 as synthesizer: about $0.50 per briefing; with Sonnet 5.5: about $0.36.
- Single agentic loop on Fable 5.2 (15 turns, context growing to ~200K, 85% cache reads, 15K output): about $2.25 cache writes + $0.26 cache reads + $0.60 output + $0.20 search ≈ $3.30, consistent with Anthropic's measured $1.49–$4.82 per deep-research task. About $6–20 a month.
- Conclusion: $1–5 per briefing; the pipeline form is 4x cheaper than the open-ended agent.

**B. Processing 1,000 documents of 10 pages**
- Assumptions: about 1,000 tokens per text page (10K per document, 10M input total), 500 output tokens per document (0.5M total). If pages are sent as PDF with page images, assume about 2.5x input (25M).

| Model | Standard (text) | Batch (text) | Standard (PDF with images) |
|---|---|---|---|
| Haiku 5.5 | $1.25 | $0.63 | $2.75 |
| Sonnet 5.5 | $25 | $12.50 | $55 |
| Opus 5.5 | $50 | $25 | $110 |
| Fable 5.2 | $100 | $50 | $220 |

- Cascade: Haiku 5.5 on everything, Sonnet 5.5 re-run on a 10% low-confidence subset: about $1.25 + $2.50 = $3.75 (batch about $1.90).
- Keep each Haiku request under 100,000 prompt tokens to avoid the 5x long-prompt price.

**C. Handling 500 support emails**
- Assumptions: 6,000-token system prompt plus knowledge base, 1,000-token thread, 800 output tokens (reply plus thinking).
- Sonnet 5.5, no cache hits (low traffic): 3.5M input × $2 + 0.4M output × $10 = $7 + $4 = $11, about $0.022 per email. With the Batch API (replies within hours): about $5.50. With a warm cache (busy inbox): about $5.30.
- Haiku 5.5 for everything: about $0.55. Haiku triage on all plus Sonnet draft on all: about $11.10. Opus 5.5 escalation for 10% of threads (10K in, 1.5K out each): add about $3.50.
- With tool calls (order lookup, refund check; about 3 model turns per email): roughly 2–3x, so $15–30 on Sonnet 5.5.
- Conclusion: $1–15 for simple replies, up to about $30 with tools; under $0.06 per email in all cases.

**D. Monitoring 5,000 tender notices a day**
- Classification by Haiku 5.5: 2,300 input tokens per notice (800 notice + 1,500 criteria), 150 output. Per day 11.5M input = $1.15 and 0.75M output = $0.38, total $1.53. Per 30-day month: about $46 standard, about $23 with Batch.
- Summarization of the top 2% (100 a day) with 15,000 input and 1,000 output tokens each: Sonnet 5.5 $4.00 a day = $120 a month ($60 batch); Opus 5.5 $240 ($120 batch); Fable 5.2 $480 ($240 batch).
- Total per month: about $83 (Haiku batch + Sonnet batch), about $166 (both standard), about $143 (Haiku batch + Opus batch), about $263 (Haiku batch + Fable batch).
- A keyword or CPV-code pre-filter in ordinary code before the model can remove most of the 5,000 notices at zero model cost.

**Monthly budget scenarios (AI + infrastructure, several micro-businesses)**

| Item | Light | Medium | Heavy |
|---|---|---|---|
| Workload sketch | 1 weekly briefing, ~300 emails, ~500 docs, a few scheduled agents | Daily briefings, ~3,000 emails with tools, tender monitoring, ~10,000 docs, ~200 agent sessions | ~20,000 emails with tools, 50,000+ docs, multi-source monitoring, ~2,000 agent sessions, browser automation |
| Model tokens (API) | $20–80 | $300–800 | $2,500–6,500 |
| Fable 5.2 supervision (weekly/daily reviews) | $5–20 | $40–120 | $200–600 |
| Web search tool | $1–5 | $10–40 | $50–200 |
| Compute (VPS / serverless) | $6–25 | $25–100 | $100–400 |
| Database | $0–25 | $25–60 | $60–250 |
| Orchestrator | $0–10 | $10–100 | $100–500 |
| Email sending | $0 | $20–35 | $90–350 |
| Observability | $0 | $0–29 | $29–200 |
| Browser automation | $0 | $20 | $99+ |
| Operator subscription (optional Max / Ultra) | $0–100 | $100–200 | $200 |
| Approximate total | $70–200 | $500–1,200 | $3,000–8,000 |

- The optional Max ($100) or Ultra ($200) seat returns $100 or $200 of API credit, which roughly covers the whole light scenario's token bill.
- Medium fits within the Build tier's $1,000 cap only at the low end; heavy requires the Scale tier. Request tier increases before launch.
- Merchant-of-record fees (5% + $0.50 per sale) are a revenue-proportional cost outside this table.
- The largest swing factor is architecture, not volume: replacing open-ended agent loops with fixed pipelines, batching non-urgent work and keeping Fable 5.2 to a handful of calls typically changes the token line by 3–10x in either direction, per the caching, batch and multi-agent multipliers in section 5.

### Gaps
- Token-per-page and tokens-per-email figures are assumptions, not measurements; run `count_tokens` on real samples before committing to a budget.
- Thinking-token overhead on Haiku 5.5 and Sonnet 5.5 for classification-style prompts was not measured; output costs could be 2–3x the assumed figures at default effort.
- PDF page token costs on current models were not verified from the PDF-support documentation.
- Scenario totals exclude human time, domain names, MoR fees, taxes, and any paid data sources or proxies.
