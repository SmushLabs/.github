# SmushChat Copilot-CTO Brief — 2026-11-02

Running notes from your async CTO. Prioritized P0 → P2. Pick 2–3 P0s this week, don't try to do everything.

---

## 1. The honest competitive read

The AI-support-widget space in late 2026 is crowded and converging: Intercom Fin, Zendesk AI, Tidio Lyro, Chatbase, Dante, CustomGPT, Botsonic, Siena, Fini, Crisp, Freshchat, HelpCrunch. Three things matter for a scrappy founder-built product like SmushChat:

1. **"Affordable" is not a moat** — Chatbase and Botsonic already win on price perception, Crisp has a free tier. You need a wedge beyond "cheaper."
2. **Your real wedge is WooCommerce + lifetime pricing + founder access.** No large player cares about WooCommerce the way you do, and nobody at Intercom will ever get on a Zoom with a $400 MRR shop.
3. **Table stakes have moved.** 2026 buyers now expect: tool/action calling (not just answers — the bot does things), voice (web + phone), returning-visitor memory, multilingual, citations, and a human-handoff inbox. Your README mentions some of this but it's not obvious on the lander.

Pick a niche. Right now the README reads "for everyone who pays Intercom too much." Everyone-is-no-one. The clearest beachhead you already have is:

> **"The AI support agent for WooCommerce stores doing $10k–$500k/mo."**

Everything below assumes you pick that or a similar wedge.

---

## 2. Feature ideas (P0 → P2)

### P0 — ship within 2–4 weeks

- **Tool/action calling, not just Q&A.** The bot should *do*: cancel order, apply coupon, resend tracking email, pause subscription. Your WooCommerce integration already has the plumbing — expose 4–6 safe actions and this becomes a genuine agent, not a chatbot. This is the single biggest 2026 differentiator vs. "trained on your PDFs" tools.
- **"Shadow mode" / Draft replies for 7 days.** Before go-live, the AI silently drafts answers the owner reviews from an inbox. Converts the scariest objection ("what if it hallucinates to my customer?") into a trust-building ramp. Chatbase doesn't do this well. Easy win.
- **$ saved counter in dashboard.** Count deflected tickets × customer's own "my support hour costs $X" input. Email a weekly digest: *"SmushChat saved you 11.2 hours and ~$340 last week."* This is your retention weapon and your testimonial generator.
- **One-click "Scan my site" demo on the lander.** Visitor pastes URL → you crawl 10 pages → spin up a sandbox chatbot answering questions about *their* site inside the hero. This is the single highest-converting pattern in this category (Chatbase, CustomGPT, Dante all do it; your lander doesn't yet based on the README).

### P1 — next 4–8 weeks

- **Returning-visitor memory.** Recognize the same browser/email across sessions and resume context. Huge for e-commerce ("did my order ship?") and almost nobody at your price point has it well-tuned.
- **Multilingual auto-detect.** Detect browser language, respond in it, keep KB in English. Opens EU + LATAM shops instantly.
- **Guardrails UI.** Let the owner write "never do X" rules in plain English and show which ones fired. Combats the hallucination fear.
- **Human-handoff inbox with pre-filled context.** When the AI punts, the human sees: visitor, cart, order history, conversation, AI's confidence, suggested reply. 60% of your "we need Intercom" churn risk disappears here.
- **A/B test on the greeting + proactive triggers.** Owners don't know what to say first. Test for them, show lift.
- **"Train from Slack / Zendesk / Help Scout export."** One-click import of historical tickets so the KB isn't just the website. This is a cold-start killer.

### P2 — on the roadmap, not now

- Voice (phone + in-widget mic). Trendy but expensive to do well; wait until you have 100+ paying customers asking.
- Native Shopify app in the Shopify App Store. High leverage but a 2–3 month build and a review gauntlet. Worth it later.
- Chrome extension that watches the owner answer live, auto-updates the KB. Magical but you don't need it yet.
- Public API + Zapier/Make integration. Fine to defer until the inbox is solid.

### What to *stop* building / cut from the lander

- "Unlimited chatbots" per account is a weak selling point and invites abuse. Replace with "unlimited conversations on one brand, extra brands at $X."
- "Lifetime updates at this tier" is risky long-term — AI inference cost is not fixed. I'd quietly cap it ("lifetime access to v1 features, future AI model upgrades at cost") before you have 500 customers you can't economically serve.

---

## 3. Landing page ideas (lander.smushlabs.ai → smushlabs.ai)

The current README reads like a Gumroad long-form page. The actual lander should do fewer things, better.

**Above the fold (test these):**
- Headline: *"The AI support agent your WooCommerce store actually needs."* (narrow) or *"Replace Intercom in 15 minutes. Keep the $2,400/yr."* (comparative anchor).
- Subhead: one sentence, resolves what/for-who/why-now.
- The *interactive* demo lives in the hero — paste-your-URL field, not a video.
- One primary CTA ("Try it on your site — 60 seconds"). Kill "Book a demo" from the hero; put it below the fold.

**Below the fold, in order:**
1. Live demo you can type into (pre-loaded with a sample store).
2. 3-step install visual (one line of code → done).
3. **Comparison table** vs Intercom / Tidio / Chatbase on 6 rows: price, lifetime option, WooCommerce actions, lifetime data ownership, human handoff, founder support. This page alone will do 30%+ of your SEO.
4. $ saved calculator. Two inputs (visitors/mo, support cost/hr), one big number.
5. A real case study — The TEFL Group's 68% number — with the actual chat transcripts, not a stat tile.
6. Founder section with your face, your Twitter, your Cal.com link. In this market the founder *is* the trust.
7. Pricing with the comparison baked in.
8. FAQ answering the real objections: hallucinations, data privacy, GDPR, "what if I cancel," model updates.

**Lander hygiene:**
- `lander.smushlabs.ai` → 301 to `smushlabs.ai` the day you cut over, don't let both index.
- Open Graph + Twitter card images with the product screenshot (not a logo).
- One pixel: Plausible or PostHog, not GA4. PostHog gives you session recording free which will teach you more about your lander than any A/B test.
- Keep TTI under 1.5s. The widget's own perf matters because prospects *will* measure it.

---

## 4. Daily social — attract founder attention, don't sell

The brief here: no "buy my product" posts. The goal is *you* become a trusted voice; the product comes along for the ride. One post a day, mix of five formats on a rotation:

**Format A — "Teardown Monday":** Public, kind teardown of one real website's support UX. Screenshot their contact page, point out 3 fixable things, say nothing about SmushChat. Weekly. Founders love being featured; this generates reply guys who become prospects.

**Format B — "Build in Public Tuesday":** One screenshot of the thing you shipped this week + the metric it moved. "Shipped shadow mode this weekend. First customer caught 4 bad answers before they went live." Real numbers > vibes.

**Format C — "Prompt Wednesday":** Share an actual system prompt you use inside SmushChat for a specific vertical (e-com, SaaS, agency). Make it copy-paste-usable even if they *don't* use your product. Over 90 days this makes you the "AI support guy" on Twitter/LinkedIn.

**Format D — "Numbers Thursday":** One honest metric. MRR, churn, support tickets deflected across all customers, infra cost per 1k messages. Founders stop scrolling for honest numbers. "This week: 1.2M messages served, $187 OpenAI bill, 2 angry customers, 1 won back."

**Format E — "Receipts Friday":** Screenshot a real customer DM/email saying something nice. Zero commentary. Or screenshot a competitor's pricing page next to yours with no caption.

Platform specifics:
- **X/Twitter** is where this ICP (indie SaaS, bootstrappers, Shopify/Woo founders) lives in 2026. Prioritize it. Build the Build-in-Public habit.
- **LinkedIn** — reformat the same post, add 2 line breaks, add one "What are you using for support?" question at the end. LinkedIn's algorithm rewards questions and dwell time.
- **Facebook** — skip personal Facebook, but a *WooCommerce Shop Owners* Facebook group presence is gold. Don't post product links; answer questions for 60 days then mention in bio.
- **Reddit** — r/woocommerce, r/ecommerce, r/SaaS, r/indiehackers. Same rule: answer questions for 60 days, then post launches sparingly.

Three post ideas you can send tomorrow:

1. *"I replaced our Intercom with the thing I'm building. One month in: 68% fewer human tickets, OpenAI bill is $23, cognitive load is 1/10th. I'll post the exact system prompt tomorrow if anyone wants it."*

2. *"Hot take: every AI chat widget is pitched as 'trained on your docs.' In 2026 that's table stakes. The real question is: can the bot actually cancel the order, resend the tracking email, apply the coupon? If not, it's a FAQ with better grammar."*

3. *"Teardown: @somesmallbrand's support page. 1) 'Contact us' form with 7 fields. 2) 48-hour response SLA buried in footer. 3) FAQ hasn't been updated since 2024. Fix the first two before you buy any software."* (choose a real brand you've bought from — tag them, make it kind)

---

## 5. Marketing tactics (ranked by expected ROI)

### P0 — do this quarter

1. **Comparison pages** — one page each: *SmushChat vs Intercom*, *vs Tidio*, *vs Chatbase*, *vs Crisp*, *vs Dante*. Fair, honest, with a "when they're better than us" row. These rank for high-intent long-tail traffic forever.
2. **AppSumo lifetime deal.** Your pricing is already compatible. One AppSumo campaign can bring 1,000+ users in 30 days, becomes your case-study factory, and the reviews live on Google forever. Downside: AppSumo tire-kickers are brutal — do shadow mode and better onboarding *before* you launch there.
3. **Product Hunt launch** after AppSumo. Lead with the interactive demo. Target top-5 of the day, not #1.
4. **Case study factory.** One per week. Fixed template: problem, numbers before, what SmushChat changed, numbers after, quote with photo. Publish on blog + LinkedIn + Twitter thread. After 12 weeks you have an un-fakeable moat of social proof.
5. **WordPress / WooCommerce agency partnerships.** Offer 30% rev share. 10 small WP agencies × 20 clients each = 200 potential installs with warm handoff.

### P1 — next quarter

6. **SEO on "AI chatbot for X"** — AI chatbot for WooCommerce, for Shopify, for TEFL schools, for marketing agencies, for law firms. Vertical pages ship fast and rank fast because competitors go generic.
7. **"Chatbot audit" lead magnet.** Free tool: paste your URL, we show the 5 questions your current support can't answer. Email-gated. This feeds a drip sequence.
8. **Guest podcasts** — My First Million, Indie Hackers, Starter Story, Shopify Masters. Pitch: "the AI tool that fired my support team in a good way." Needs a strong case study first.
9. **Twitter/LinkedIn ads on comparison keywords** — "intercom alternative," "tidio alternative." $500/mo test budget, send to comparison pages.
10. **Referral program.** 30% recurring commission or lifetime. Make it visible in the dashboard. Your existing customers *are* founders — they have other founder friends.

### P2 — later

- A YouTube channel ("I built an AI support agent for X") — high effort, slow payoff. Only if you enjoy video.
- Paid Google Ads on brand terms (defensive, when competitors start bidding on "SmushChat").
- A conference booth. Not until $20k MRR.

---

## 6. Engagement / retention

Acquisition without retention is a hamster wheel. These compound:

- **Week-one activation email sequence** — 5 emails: install, train, go live, first win, "did you see your weekly report?" Hand-write them, don't templatize until you have 100+ customers.
- **Weekly value digest** (the $ saved email). This is your anti-churn drug.
- **Public roadmap with voting.** You mention this. Make it real, link it in-app and from the lander. Customers who vote stay 3× longer.
- **Monthly office hours.** Zoom, 45 minutes, you + any customer. Record the Qs → become FAQ → become blog posts.
- **A real changelog page** (`/changelog`). Update weekly. Email it. Changelog pages compound SEO and reduce churn — customers see motion.
- **Loom from the founder** on day 3. Record a personal 60-second Loom to each new paid signup. Does not scale past 50 signups/day; by then it won't matter.

---

## 7. What I'd actually do this week if I were you

Not everything. Pick these five:

1. Decide the wedge (WooCommerce? agencies? both? one of them, written on the wall).
2. Add the paste-your-URL interactive demo to the hero of the lander. This moves conversion more than any other single change.
3. Start Build-in-Public on X. Three posts, formats A/B/C above. Pin a thread about why you're building this.
4. Ship Shadow Mode as a feature flag for 3 willing beta customers. Collect quotes.
5. Draft the Intercom and Tidio comparison pages. Publish within 10 days.

Everything else — AppSumo, voice, Shopify app, podcast tour — queues behind these.

---

## 8. Risks to keep an eye on

- **Lifetime pricing + rising inference cost** — do the napkin math per customer. One heavy user on a lifetime plan can quietly go negative margin. Add a soft fair-use cap now, before you have 1,000 of them.
- **OpenAI/Anthropic model deprecations.** Build a provider abstraction (Opus/Sonnet/GPT/Gemini) now so you can swap without customer-visible changes.
- **Data residency / GDPR.** As soon as one EU customer asks, you need an answer. Pick a region strategy and write the one-page policy *before* a prospect asks and you lose the deal.
- **Impersonation risk.** As soon as "SmushLabs" has any name recognition, someone will squat SmushChat.io, SmushChat.ai, @SmushChat on IG. Grab the handles this week — $12 of domains is cheap insurance.

---

Next brief: I'll come back with specific KPI targets and a 90-day plan once you tell me the wedge.
