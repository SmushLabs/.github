# SmushChat Copilot-CTO Brief — 2026-10-20

For: Asif, Founder @ SmushLabs
Scope: SmushChat (AI customer support widget). Lander moving `lander.smushlabs.ai → smushlabs.ai`.
Format: things to do this week, with the "why" compressed. Pick 2–3, not all.

---

## 1. The one thing to fix on the landing page this week

**Add an "actually working" interactive demo above the fold.**
Right now the README reads like a feature list ("intelligent AI… natural language… remembers context"). Founders have seen that copy a thousand times. The thing that converts is: *they type into a real widget on your lander and watch it answer a hard question about SmushLabs itself*.

- Minimum version: embed the SmushChat widget on `smushlabs.ai`, trained on your own docs + a canned list of 10 tough questions ("what if my docs are in 3 languages?", "can it refuse to answer off-topic?", "show me how it hands off to a human").
- Add a visible "Try these questions" chip row so visitors don't stare at a blank input.
- This is also the single best piece of content for a Twitter/LinkedIn post ("the chatbot on our site is the product — ask it anything").

Everything else on the page (pricing, logos, comparison table) matters less than this one interaction working flawlessly in the first 10 seconds.

## 2. The TEFL Group case study is undermonetized

You have "12,000+ monthly visitors, 68% reduction in support tickets" sitting in the README as a bullet. That is a complete marketing asset waiting to be unpacked:

- **Dedicated case-study page** (`/customers/tefl-group`): the before (what tickets looked like), the setup (how it was trained, how long), the after (ticket volume chart, time-to-first-response, specific question types deflected), one quote.
- **Teardown video (3–5 min, screen recording, no face required):** "here's exactly how we cut TEFL's tickets by 68%". Post to LinkedIn, YouTube Shorts, Twitter.
- **Numbers to pull out as standalone social posts**: "A single ~$X/mo widget replaced ~Y hours/week of human support at a 12k-visitor site. Here's what it took to set up." Each number is a post.

Founders don't buy from feature lists. They buy from "someone like me got this result."

## 3. Daily social cadence — the "founder-attention" track, no selling

Rough skeleton. Pick one lane per day, keep it short, never pitch at the end.

| Day | Lane | Example |
|---|---|---|
| Mon | Benchmark | "I pulled 30 days of chatlogs across 7 SmushChat sites. 54% of questions were just 'where's my order' variants. Here's the exact phrasing." |
| Tue | Build-in-public | "Shipped multi-language detection today. The ugly part: our fallback kept defaulting to Spanish because of a bad test fixture. Here's the fix." |
| Wed | Teardown | "I tried to break 5 competitor chatbots with the same question. Here's what each said and what it reveals about their training." (Intercom Fin, Tidio Lyro, Chatbase, Crisp, Drift) |
| Thu | Framework | "A 4-step framework for deciding if your business should run a chatbot at all. If you fail step 2, don't bother." |
| Fri | Behind-the-scenes | A screenshot of the live inbox, metrics, or a pricing-page draft — ask followers which version to ship. |
| Sat | Lesson | A mistake you made running an agency / building for TEFL. The specifics make it believable. |
| Sun | Vision | One paragraph on where support is going (agents acting on behalf of users, not just answering). |

Rule: no "DM me", no "book a demo", no "SmushChat is… ". The product gets mentioned by name twice a week max. Attention compounds; sales posts don't.

For LinkedIn specifically: lead with a line break after the first sentence (the "hook" line is the only thing visible pre-expand), and end with one question that invites a reply. The algorithm feeds posts whose first comment comes within 10 minutes — ask someone on the team (or a founder friend) to reply first.

## 4. Three feature ideas worth prototyping this quarter

Ranked by (user pain) × (differentiation vs. Intercom/Tidio/Chatbase):

**a. "Train from your existing support tickets."**
Most competitors train from a URL + PDF upload. The real goldmine is a merchant's existing Zendesk/Freshdesk/Gmail support history. A CSV uploader + an opinionated ingestion pipeline ("we'll find your top 50 question clusters and build a Q&A set from the actual replies your team sent") is a sharp wedge. It also surfaces a report ("here's what your team is spending time on") which is itself a conversion asset — merchants will share it internally.

**b. "Suggest reply" inside the human-takeover inbox.**
When a human agent takes over, SmushChat should still be *writing drafts* beside the input box, Copilot-style, learned from past agent replies on this account. This is how Intercom's "Fin for agents" product is being sold at $35/seat/mo. You can match it with the data you already have.

**c. Appointment booking inline.**
A huge class of SMB sites (dentists, lawyers, agencies, salons) wants the chatbot to end the conversation with a booked slot, not a redirect to Cal.com. A single integration with Cal.com + Google Calendar + an inline time-picker rendered inside the chat bubble is table-stakes for the service-business segment and is weak-to-missing in Chatbase/Tidio.

Deliberately not pursuing yet: voice I/O (cool, but <2% of customer-support traffic), full computer-use agents (too far ahead of the ICP).

## 5. Competitor map — where SmushChat can credibly win

| Competitor | Where they're strong | Where they're weak (your opening) |
|---|---|---|
| **Intercom Fin** | Brand, enterprise sales, Resolution-based pricing | $0.99/resolution adds up fast; setup is a sales cycle; overkill for sub-$10M ARR shops |
| **Tidio / Lyro** | Shopify integration, free tier | Lyro limited to 50 convos/mo on cheap plans; AI feels last-gen; limited customization |
| **Chatbase** | Fast setup, developer-friendly, ChatGPT-style training | Shallow e-commerce integrations; no human-takeover inbox worth using; no WhatsApp |
| **Crisp** | Price, multi-channel inbox | AI is bolted-on, not core; UX is cluttered |
| **Drift** | Enterprise B2B, pipeline-focused | Not for SMB; expensive; e-commerce not the ICP |
| **Voiceflow / Botpress** | Builder flexibility | Requires building; not plug-and-play |

**SmushChat's defensible wedge:** price + e-commerce depth (WooCommerce order tracking, product recs) + WhatsApp + "founder built, not VC built" trust. Lead with that wedge in every piece of positioning. The one thing I would *add* to the current README: a direct comparison table against Tidio and Chatbase (the real alternatives your ICP is weighing), not Intercom (which they can't afford anyway).

## 6. Two small landing-page wins (do these alongside the demo in §1)

- **Replace the "What makes SmushChat different" ❌/✅ block** with a side-by-side table against *named* competitors (Tidio, Chatbase, Intercom). Founders are already comparing — do the work for them. Vague "other tools" copy reads like you can't name a competitor.
- **Add a "set up in 12 minutes" live screencast** (muted, autoplay, 60s) in the "Easy Setup" section. The 5+5+2 minute breakdown is more credible when you can see it happen.

## 7. Engagement loops to build this month

- **Public changelog on the lander** (`/changelog`). Ship weekly, link each post from a tweet. Shipping velocity is itself a trust signal for founders choosing between you and a VC-backed tool that updates quarterly.
- **"Feature Roadmap" voting** is already mentioned in the README — but the link is missing (`cal.com/20min` is only the demo). Wire up a public Canny or GitHub Discussions, and *post the top vote weekly* on social. Turns users into co-authors.
- **Free "chatbot ROI calculator"** on the lander. Visitor inputs: monthly visitors, avg tickets/mo, avg time per ticket, support staff cost. Output: dollars saved + a "share your result" image. Zero-friction lead magnet.

---

## Suggested next 7 days (if I were sequencing it)

1. **Mon** — ship interactive demo on lander (§1)
2. **Tue** — write the TEFL case study page (§2); post Mon's benchmark
3. **Wed** — competitor teardown post (§3 Wed lane); start ROI calculator
4. **Thu** — ship changelog page; publish framework post
5. **Fri** — ship ROI calculator; post asking which pricing-page variant to go live with
6. **Sat–Sun** — write the "train from existing tickets" spec (§4a), scope for engineering

If only one thing from this brief ships this week, make it §1 (interactive demo on the lander). It compounds into every social post and case study after it.

— generated by scheduled Copilot-CTO run
