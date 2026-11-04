# SmushChat Copilot-CTO Brief — 2026-11-04

Working from the current profile README (positioning: "AI customer support widget, founder-priced, WooCommerce + WhatsApp friendly, lifetime tier available"). Landing page `lander.smushlabs.ai` was not reachable from this session's network policy, so the landing-page section below is based on the README copy. Allowlist the domain if you want the next brief to audit the live page.

---

## 1. Competitive landscape — where the moat actually is

| Tool | 2026 price signal | Where SmushChat wins | Where SmushChat is behind |
|---|---|---|---|
| **Intercom Fin** | ~$0.99 per resolution + seat fees | Flat/lifetime price, no per-resolution meter | Fin brand trust, workflow builder depth, marketplace apps |
| **Tidio Lyro** | ~$39/mo for 50 AI convos, then steep | Unlimited conversations story | Shopify-native checkout flows, built-in email marketing |
| **Chatbase** | ~$32/seat/mo, credit meter | Full control, lifetime pricing, human-takeover inbox | Larger template library, more public case studies |
| **SiteGPT** | ~$49/mo | WooCommerce order-tracking tool-call | Faster onboarding video, slick quick-start |
| **CustomGPT** | ~$99/mo | Cheaper, WordPress-native | Robust public API, enterprise-grade RAG posture |
| **Zendesk AI Agent** | ~$1.50 per resolution | Price, founder-direct support | Ticketing platform depth, SSO/SAML, compliance |

**Three gaps you can own in the next 60 days:**

1. **Flat-fee "unlimited" promise with a receipt.** Everyone else meters now. Publish a live counter on the landing page: "Conversations handled this month across all customers: 418,221. What that would have cost on Fin at $0.99: $413,938." Even a static monthly screenshot works.
2. **WooCommerce + WhatsApp as a wedge.** Chatbase/CustomGPT barely touch these; Tidio owns Shopify. Position SmushChat as "the WooCommerce + WhatsApp chatbot" in one lane instead of fighting on general-purpose terms.
3. **Founder-direct onboarding.** Keep the 30-min call. That's your 4.9-star-review generator and the thing a $200M-ARR Intercom literally cannot match.

---

## 2. Feature ideas (ranked by effort × wedge)

**Ship in next 2 sprints (high leverage, low build cost):**
- **MCP tool support** — expose a bot's toolset (order lookup, refund status, inventory check) as an MCP server. Lets the chatbot plug into Claude Code, ChatGPT, Shopify admin, etc. A single README line "MCP-ready" would set you apart from everyone except Intercom.
- **Deflection ROI report, auto-emailed weekly.** "This week SmushChat answered 847 questions. At Intercom pricing that would have cost $838." This is the single email that keeps customers from churning.
- **"Draft reply" mode for live chat.** The AI drafts, the human sends with one click. Converts the "I don't trust full automation" segment.
- **Install-verification check.** When they paste the script tag, a widget on the dashboard confirms the site is sending heartbeats. Cuts support tickets and no-show onboarding calls in half.

**Ship this quarter (differentiators):**
- **Voice mode for the widget** (mic button → speech-to-text in → spoken reply out). 2026 chatbots are expected to be multimodal; this is table stakes by Q2.
- **Shopify-native app listing.** Everyone focuses on WordPress. Shopify's app store is where the WooCommerce comparison closes.
- **"Train on competitor pricing page" templates.** Pre-built starter packs: SaaS pricing bot, agency portfolio bot, educator Q&A bot, e-commerce returns bot. Ship as one-click presets with sample sources + persona + colors.
- **Human handoff via WhatsApp.** When the bot gets stuck, it DMs the founder's personal WhatsApp with the transcript and a "reply here to continue" hook. Founders will pay for this.

**Think about but don't start yet:**
- Multi-agent orchestration (one bot per department, router agent on top). Big build, uncertain demand at your price point.
- On-device/edge model option. Only matters if you land an enterprise buyer.
- Custom model fine-tune per account. Expensive to support; RAG + prompt is 95% of the value.

---

## 3. Landing-page changes (based on README copy)

Swap the current hero's "Stop Losing Customers to Unanswered Questions" for something more measurable. Generic pain-point headlines are the Chatbase/Tidio formula; you need to look different.

**Hero rewrite to A/B test:**
> **"Pay $X once. Answer every customer question forever."**
> **"The chatbot Intercom charges $0.99 per answer for — flat-priced, built by a founder you can actually talk to."**

**Sections to add in order of ROI:**
1. **Live cost-comparison calculator.** Slider: "How many support questions per month?" → shows SmushChat flat price vs. Fin/Lyro/Chatbase running total. This converts.
2. **Loom-style 90-second demo at the top, autoplay muted.** The current page is text-heavy; founder audiences skim. Record you using your own bot on your own site.
3. **"Built with these models" strip.** Logos of the model providers under the hood (if you want to be transparent) or just "Powered by frontier LLMs, swappable per account" — reassures the technical buyer.
4. **Public roadmap embed.** You already promise "users vote on features." Embed the actual Canny/Featurebase widget on the page. Converts fence-sitters into trial users because they want a say.
5. **Comparison table** — the one from section 1. Rename columns to ✅/❌ on 6 criteria (flat price, unlimited convos, WhatsApp, WooCommerce, human handoff, founder support).
6. **Founder video testimonial carousel.** Three 20-second clips from TEFL Group + two more. Text testimonials are discounted; video isn't.
7. **"Install in 60 seconds" live sandbox.** A fake e-commerce store on the page where the widget is already running — visitors can chat with it before signing up.

Remove or shorten:
- The "What Happens After Purchase" section is a trust-builder but it's below the fold — tuck it into a collapsible FAQ.
- The feature list is good but currently reads as 7 equally-weighted bullets. Pick the three the buyer actually chooses on (price, WooCommerce/WhatsApp, lifetime) and make them the top of the fold.

---

## 4. Daily social posting plan — attract, don't sell

**North-star rule:** 4 out of 5 posts should have zero mention of SmushChat. The one that does should be a specific build-in-public update, not a "buy now."

**Weekly rotation (adapt daily):**

- **Mon — Build-in-public.** What you shipped last week, what you're shipping this week, one number. Example: *"Last week: WhatsApp handoff shipped. 11 customers turned it on in 48h. This week: I'm adding MCP tool calls so your chatbot can work inside ChatGPT. Why: because in 18 months every customer-support tool will be an MCP endpoint, and I'd rather be early than right."*

- **Tue — Teach.** A specific tactic another founder can steal, from your own work. Example: *"Most founders paste their whole FAQ into their chatbot and wonder why answers are mush. Try this instead: one doc per intent ('refunds', 'shipping delays', 'product X compatibility'). Chunking by intent cut our customers' hallucination reports by ~70%."*

- **Wed — Teardown.** Pick a competitor's pricing page or landing and write what's broken. No naming your tool. Example: *"Intercom just raised Fin to $0.99 per resolution. A store doing 10k support convos a month is now paying $9,900 for an AI that costs them ~$200 in tokens. The arbitrage will not survive 2027. Here's what I'd do if I were them →"*

- **Thu — Customer story.** One customer, one specific number, one quote. No logo-walls, no "trusted by." Example: *"@TEFLGroup had 12k monthly visitors and a 2-person support team drowning in 'where's my order' tickets. 60 days later: 68% fewer tickets, same team, 0 extra tooling. Full story + the exact training setup they used →"*

- **Fri — Founder-life / opinion.** Spicy but true. Example: *"I spent 2 years building chatbots for clients at $5k/each. The dirty secret: 80% of what they paid for was configuration I could have shipped as defaults. That's why SmushChat exists. Also: if your tool requires a 'solutions engineer' to configure, it's not AI, it's a config wizard with a chat UI."*

- **Sat — Short-form useful.** A single-sentence insight or 1-image carousel. Lower lift, keeps cadence.

- **Sun — Engagement.** No post. Spend 45 minutes commenting substantively on 10 other founders' posts. This is where LinkedIn's algorithm boosts you for the next week.

**Platform-specific adjustments:**

- **LinkedIn:** the above rotation, 1 post/day, 150–250 words, a specific number in line 1, the key insight in line 2, the rest below the "see more" fold. No hashtag spam — 3 max.
- **X/Twitter:** same content, chopped into threads. X is where build-in-public still lives. Post the Mon/Wed/Fri variants as 4–7-tweet threads. Reply to 3 bigger founders' tweets per day.
- **Facebook:** lowest leverage for a B2B founder tool. Post only Mon and Thu. If you have WooCommerce/Shopify/WordPress founder groups, post Thu's customer story there — it converts at 5-10x LinkedIn for e-com buyers.

---

## 5. Marketing tactics with asymmetric upside

1. **Programmatic SEO on competitor comparison pages.** Build `smushlabs.ai/vs/intercom-fin`, `/vs/tidio-lyro`, `/vs/chatbase`, `/vs/sitegpt`, `/vs/customgpt`. Each page: 800 words, honest comparison, your advantages last, cost calculator embedded. Target "chatbase alternative", "intercom alternative" — these keywords convert because the searcher is already paying someone and unhappy.
2. **List on AppSumo as a one-time lifetime deal.** AppSumo is tailor-made for your flat-price positioning. Even at 70% rev share it's a 2–3k install pipeline and years of SEO backlinks.
3. **Free WordPress plugin, premium backend.** Ship a `smushchat` WordPress.org plugin that works with a free-tier account (100 conversations/mo). The WordPress.org listing itself is a top-10 organic result for "ai chat" queries.
4. **Side-project backlinks.** Ship 2–3 free micro-tools under smushlabs.ai subpages: "Chatbot ROI calculator," "AI customer support cost estimator," "WooCommerce support benchmark report." Each one is a link magnet and each one feeds leads into the main funnel.
5. **Directory listings (weekend task).** Product Hunt relaunch, G2, Capterra, SaaSHub, There's An AI For That, Futurepedia, AI Tool Guru. Roughly 20 directories, ~4 hours total. Each one is a backlink + a small lead trickle.
6. **LTD community partnerships.** PitchGround, StackSocial, DealMirror — specifically target their e-commerce audiences. One well-timed LTD run can bootstrap you to 2–3k lifetime customers in a week.
7. **Agency reseller tier.** Agencies managing 20+ WordPress sites will pay 3–5x retail for a white-label reseller account. Low-volume, high-margin, zero acquisition cost once the first agency is in. Message: "Charge your clients $99/mo, pay me $29/mo, keep the delta."

---

## 6. Engagement loops you can bolt on

- **In-product referral link.** Every paying customer gets a URL. One signup via that URL → 30 days free. This is cheap and underused in LTD SaaS.
- **Embeddable "Powered by SmushChat" leaf** (opt-out on paid plans, default-on on free). Every free widget running on a real site is a mini-billboard.
- **Monthly customer office hours.** 45-min Zoom, you demo new features, customers ask anything. Record, cut into clips, post. This feeds section 4's content rotation for free.
- **A weekly email: "What your bot did this week."** Deflection count, top 3 unanswered questions (= knowledge gaps), top 3 user intents. Makes churn harder every week it ships.

---

## 7. What to do this week (concrete)

1. Pick **one** feature from section 2's top list. My bet: **install-verification + weekly ROI email** — both are 2-day builds and both directly prevent churn.
2. Draft **one** comparison page from section 5. My bet: `/vs/intercom-fin` — highest search volume, most mismatched price point.
3. Record **one** 90-second product demo video. Loom, unlisted, embed on the homepage above the fold. You can replace it monthly.
4. Post Mon + Wed + Fri on LinkedIn from section 4's templates. Three posts, not seven. Consistency later; start now.
5. Unblock `lander.smushlabs.ai` in this session's network settings so the next brief can audit the live page instead of the README.

---

*Next brief: 2026-11-11. If you want a different slice of this covered in more depth (e.g. "just the X thread templates" or "deep dive on the WooCommerce wedge"), reply on the trigger and I'll reshape next week's run.*
