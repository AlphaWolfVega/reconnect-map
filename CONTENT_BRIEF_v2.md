# RECONNECT MAP — CONTENT BRIEF V2

**Status:** Awaiting Alpha validation + 6-agent audit before code.
**Build:** 2026-05-07
**Audience:** English-speaking adult women, Australia primary market.
**Routes to:** Pleasuary Elysia (V1) — toggleable to POPPY in 1 line.

---

## 0. STRATEGIC FRAME

**Headline (validated):** *There are 5 kinds of pleasure. Most women only ever experience two. Find out which one is yours — and which one is missing.*

**Sub (validated):** *Take 90 seconds. Find out which two are yours — and which three you've never met.*

**CTA (validated):** *Show me where I am →*

**Big Idea (Schwartz):** Pleasure is not a binary (have/don't have). It is composed of 5 distinct sensations. Most women only experience 1–2 because most devices stimulate one zone. Reaching all 5 requires three coordinated stimulations simultaneously — which is exactly what Elysia is built for.

**Voice:** Direct, sensual but classy, peer-to-peer, never clinical, never condescending. Australian English (recognise / behaviour / colour). No moralising. No shaming. The reader leaves the test feeling smarter about herself, not pitched at.

---

## 1. THE 5 KINDS OF PLEASURE

| # | Name | Sensation | Physiological mechanism | Elysia stim that delivers it |
|---|------|-----------|-------------------------|--------------------------------|
| 1 | **The Strike** | Focal, immediate, sharp peak | Direct clitoral stimulation, fast nerve response | Clitoral pulses |
| 2 | **The Slow Burn** | Anticipation, rising heat, presence | Parasympathetic ramp, low-intensity prolonged | Emerges when 3 stims start gentle + cortisol drops |
| 3 | **The Tide** | Deep, internal, rolling rising-falling waves | G-spot + internal zone response | Back-and-forth internal motion |
| 4 | **The Hum** | Full-body, ambient, enveloping, off-zone | Diffuse vibration response across nervous system | Enveloping vibration |
| 5 | **The Echo** | Post-peak afterglow, integration, surrender, still | Integrated nervous-system response after multi-zone stim | Emerges only when all 3 stims fire simultaneously |

**The mechanism phrase (used in every verdict):**
> "Most devices stimulate one zone. One zone gives you 1, maybe 2 of these. Reaching all five requires three coordinated stimulations simultaneously — which is exactly what Elysia is built for."

---

## 2. ARCHITECTURE — CONDITIONAL FLOW

```
Q1 (AGE — always asked first, gates the path)
        ↓
   ┌────┼────┬────┬────┐
   ↓    ↓    ↓    ↓    ↓
PATH PATH PATH PATH PATH
  A    B    C    D    E
18-29 30-39 40-49 50-59 60+
   │    │    │    │    │
   └────┴────┴────┴────┘
        ↓
  COMMON QUESTIONS (8) — same for all paths, measure 5 pleasures
        ↓
        Result page (verdict assembled from age opener +
        profile narrative + mechanism + bundle reco OR soft exit)
```

**Total per user:** Q1 (age) + 3-4 path-specific questions + 8 common questions = **12-13 questions**.

---

## 3. QUESTION 1 — AGE (always first)

**Prompt:** *Before we begin — what's your age range? The map adjusts to where you are.*

**Helper:** *We ask first because the body and the questions both differ across decades. Honest answer is the most useful.*

**Options (radio):**
- 18–29
- 30–39
- 40–49
- 50–59
- 60+

**Routing:** Q1 answer → assigns path A/B/C/D/E for the next 3-4 questions, then merges into the 8 common questions.

---

## 4. PATH-SPECIFIC QUESTIONS (3-4 per path)

### PATH A — 18–29 (Exploration / Discovery)

**A1.** Are you in a relationship right now?
- Yes, long-term
- Yes, recent or new
- No, single
- It's complicated

**A2.** How would you describe your experience with intimate exploration so far?
- I've explored quite a bit and know what I like
- I've tried a few things, still figuring it out
- I'm just starting to figure it out
- Honestly, very little

**A3.** What's pulling you to take this test?
- Discovering what works for me
- Reconnecting with my body after a stressful period
- Building confidence in what I want
- Curiosity — I just want to know

**A4.** *(Slider 0–10)* When did you last feel really, truly comfortable in your own body?
- 0 = honestly I'm not sure I ever have / 10 = today

---

### PATH B — 30–39 (Pressure / Reality)

**B1.** Which of these describe you right now? *(multi-select)*
- In a long-term relationship or marriage
- With young children (0–5 years)
- Recently postpartum (within last 18 months)
- Single or recently single
- In a career-intense phase

**B2.** Stress level the past 6 months:
- Manageable
- Heavy but I'm coping
- Constant — it's been a year or more
- Honestly, off the scale

**B3.** Has your relationship to your own body shifted?
- I feel disconnected from it
- I feel like I don't recognise it
- It's still mine, just different
- It feels okay

**B4.** When did you last have time, alone, just for yourself?
- This week
- This month
- I honestly can't remember
- Don't make me think about it

---

### PATH C — 40–49 (Transition / Perimenopause)

**C1.** Where are you with perimenopause? *(periods irregular, hot flushes, sleep disrupted, mood shifts...)*
- Not yet — it hasn't started
- Yes — symptoms started in the past year
- Yes — I've been in it for a while
- I'm not sure

**C2.** Has your drive, desire or sensitivity shifted noticeably?
- Yes, and I don't like it
- Yes, but I'm not sure how to feel about it
- A little, but it's manageable
- No, not really

**C3.** Has anyone (doctor, friend, partner) said this is "normal at your age"?
- Yes, and I half-believe it
- Yes, and I don't believe it
- No, I haven't talked about it with anyone
- I've never thought of it that way

**C4.** Which word fits the past six months best?
- Tired / Disconnected / Fine / Numb / Okay / Invisible

---

### PATH D — 50–59 (Menopause + Resignation)

**D1.** Where are you with menopause?
- Postmenopause (12+ months without a period)
- Late peri — unpredictable
- I'm not sure

**D2.** Has your doctor told you "it's normal at your age"?
- Yes, no real solution offered
- Yes, with HRT or similar prescription
- No, they took it seriously
- I haven't asked

**D3.** Which sentence is closest to how you talk to yourself at 1am?
- "I'm managing this phase fine."
- "My drive is gone and I miss it."
- "It's just life after 50."
- "My intimate life feels over."
- "I want to feel alive in my body again."

**D4.** Have you tried something already? *(multi-select)*
- HRT
- Lubricants or moisturisers
- Talk therapy or counselling
- An intimate device — it didn't deliver
- Nothing yet
- Something else

---

### PATH E — 60+ (Repositioning / Late discovery)

**E1.** Your relationship status:
- Long partner, sexually active still
- Long partner, intimacy has faded
- Widowed
- Divorced or separated
- Single by choice

**E2.** How long since you felt fully alive intimately?
- Less than a year
- 1–3 years
- 5+ years
- I honestly can't remember

**E3.** Your relationship with your body now:
- I've made peace with where it is
- I miss who I was
- I'd like to feel something again, even occasionally
- I'd rather not think about it

**E4.** Have you ever wondered if it's still possible at your age?
- Yes, often
- Sometimes
- I've decided it isn't
- I haven't let myself wonder

---

## 5. COMMON QUESTIONS (8 — same for all paths)

These measure the 5 pleasures. Scoring rules below the questions.

**Q-COMMON 1.** When you imagine a deeply satisfying intimate moment — does it land in one focused spot, or does it spread out across your body?
- Sharply focused on one spot
- Mostly focused, with some spread
- Spread evenly through the body
- Both — depends on the moment
- I haven't thought about it that specifically

**Q-COMMON 2.** Which speed feels closest to what your body actually wants?
- Quick and intense — get there
- Steady and rising — let it build
- Slow and deep — make it last
- Variable — depends on the day

**Q-COMMON 3.** Where do you feel most alive — externally (skin, surface) or internally (deeper, lower)?
- External, surface, skin level
- Internal, deeper
- Both equally
- I'm not sure

**Q-COMMON 4.** When you think about pleasure, where does your mind go?
- The peak itself, the moment
- The build-up, the anticipation
- The afterglow — how I feel after
- All of it equally

**Q-COMMON 5.** Vibration — what's your relationship with it?
- Yes, more is better
- Specific kinds only — I'm picky
- Not really my thing
- I haven't experienced real, well-designed vibration

**Q-COMMON 6.** How important is being able to let go completely (not having to think about anything during)?
- Essential — if I can't, nothing happens
- Helpful but not required
- I prefer staying present and aware
- I've never really let go

**Q-COMMON 7.** Which sensation have you experienced — and recognised as truly *yours*? *(multi-select, max 5)*
- A sharp, focused peak (Strike)
- A slow rising heat that built and built (Slow Burn)
- A deep, rolling internal wave (Tide)
- A full-body hum or tingling (Hum)
- A long, integrating afterglow (Echo)
- I'm honestly not sure I've felt any of these clearly

**Q-COMMON 8.** Which sensation have you wondered about, or been curious about, but haven't really had? *(multi-select, max 5)*
- A sharp, focused peak (Strike)
- A slow rising heat that built and built (Slow Burn)
- A deep, rolling internal wave (Tide)
- A full-body hum or tingling (Hum)
- A long, integrating afterglow (Echo)
- None — I'm content with what I have

---

## 6. SCORING — WHICH 2 PLEASURES ARE HERS, WHICH 3 ARE MISSING

For each of the 5 pleasures, compute a 0–10 score from the answers:

| Pleasure | Boosted by (+) | Reduced by (−) |
|----------|----------------|------------------|
| **Strike** | Q-C1 "focused", Q-C2 "quick", Q-C3 "external", Q-C4 "the peak", Q-C7 includes Strike | Q-C1 "spread", Q-C2 "slow" |
| **Slow Burn** | Q-C2 "steady"/"slow", Q-C4 "build-up", Q-C6 "essential"/"helpful", Q-C7 includes Slow Burn | Q-C2 "quick", Path E2 "5+ years" |
| **Tide** | Q-C3 "internal", Q-C2 "slow and deep", Q-C7 includes Tide | Q-C3 "external" only |
| **Hum** | Q-C1 "spread", Q-C5 "yes more"/"specific", Q-C7 includes Hum | Q-C5 "not my thing" |
| **Echo** | Q-C4 "afterglow", Q-C6 "essential", Q-C7 includes Echo | Q-C6 "never let go" |

**Hers (vécus):** Q-C7 multi-select gives the explicit "yes I've had this" baseline. Combined with high scores from C1-C6, we identify the 1–2 dominant pleasures.

**Missing:** Q-C8 multi-select gives explicit "wondered about". Combined with low/zero scores, we identify the 3 missing.

**Edge case — "she's already there":** If Q-C7 = 4 or 5 selected → trigger soft exit (A) "you're already there".

**Edge case — "she's at zero":** If Q-C7 = 0 selected AND age path indicates exploration (A) → ask whether she'd like a starter recommendation rather than full Elysia pitch.

---

## 7. VERDICT — MODULAR ASSEMBLY

Each verdict is assembled from 4 modules:

```
[AGE OPENER (1 of 5)]
    +
[PROFILE NARRATIVE (1 of 5 — based on dominant pleasure)]
    +
[MECHANISM EXPLANATION (universal)]
    +
[BUNDLE RECO (Spark or Wildfire)]
```

### 7A. AGE OPENERS

**Path A (18–29):**
> *You're at the start. Most women your age are still discovering what their body responds to — and most never get a clear map of it. Yours is below.*

**Path B (30–39):**
> *Your decade is the most under-reported in our verbatims. Stress, kids, careers, postpartum — they don't show up on a doctor's chart but they show up everywhere else. Including here.*

**Path C (40–49):**
> *Perimenopause shifts the map underneath you, often before anyone names it. The good news: the shift is mappable, and most of what you're feeling is more reversible than you've been told.*

**Path D (50–59):**
> *Most women in your decade have been told some version of "it's just life now". The map below is the second opinion you didn't get.*

**Path E (60+):**
> *Most diagnostics never address your decade honestly. We do. The map below was built knowing exactly who's reading it.*

### 7B. PROFILE NARRATIVES (5 — based on dominant pleasure)

**Profile = THE STRIKE (focal peak)**
> Lead: *You know **The Strike**. The sharp, focused peak. Most women who score this way also know **The Hum** or **The Tide** — but rarely all three.*
>
> Body: Your map suggests your body responds quickly and clearly to focused stimulation. That's a gift — it means the response system is intact. What's missing isn't the response. It's the range.
>
> Bullets:
> - **What you have:** A reliable, focused peak. Most women never get a clear one.
> - **What's missing:** The slow build-up, the deep internal wave, the integrating afterglow. Most women never know these exist as distinct experiences.
> - **Why:** Devices that deliver The Strike are everywhere. Devices that deliver all five are not.

**Profile = THE SLOW BURN (anticipation, presence)**
> Lead: *You know **The Slow Burn**. The rising heat. The presence. The way time slows down before anything has even happened.*
>
> Body: Your map suggests you live more in the build than in the peak — and that's actually rarer and harder than the peak itself. It requires a parasympathetic nervous system that knows how to drop, which most women's never quite gets to.
>
> Bullets:
> - **What you have:** Presence + anticipation. The hardest of the five to access. Most women rush past it.
> - **What's missing:** The Strike (focal release), The Tide (internal wave), The Echo (the integrating afterglow that the build was preparing for).
> - **Why:** You've trained the build but no device coordinated the rest. Build without release becomes its own kind of stuck.

**Profile = THE TIDE (deep, internal)**
> Lead: *You know **The Tide**. The deep internal rolling. The wave that rises and falls inside you, not in one spot.*
>
> Body: Your map suggests internal sensitivity and a body that responds to depth — not surface. This is the rarer half of the response system, and the half most external-focused devices ignore entirely.
>
> Bullets:
> - **What you have:** Deep internal rolling response. Half the women in our verbatims have never identified this as distinct.
> - **What's missing:** The external Strike, the parasympathetic Slow Burn, the full-body Hum.
> - **Why:** A device that delivers The Tide alone leaves the surface, the build, and the wider body unaddressed.

**Profile = THE HUM (full-body, ambient)**
> Lead: *You know **The Hum**. The full-body ambient response. Pleasure that doesn't sit in one zone — it spreads.*
>
> Body: Your map suggests a nervous system that responds diffusely and broadly. That's a rare wiring, and it explains why most one-zone devices have left you flat — they were aimed at the wrong target entirely.
>
> Bullets:
> - **What you have:** Full-body diffuse response. Often described as "tingling" or "wave that wraps around you".
> - **What's missing:** The focal Strike, the rising Slow Burn, the deep internal Tide.
> - **Why:** Your wiring needs the *combination* of all three stims simultaneously — vibration alone or pulses alone leaves the others dark.

**Profile = THE ECHO (afterglow, integration)**
> Lead: *You know **The Echo**. The afterglow. The integration. The way your body settles into itself after.*
>
> Body: Your map suggests you experience pleasure as much in what comes after as in what comes during. This is the most sophisticated of the five and also the most overlooked — most women never name it as a distinct pleasure at all.
>
> Bullets:
> - **What you have:** The afterglow. The settling. The integration. The reason most women describe pleasure as "feeling like myself" rather than "the climax".
> - **What's missing:** The actual climaxes that produce the Echo — Strike, Slow Burn, Tide, Hum. The afterglow without the multi-zone build is a half-experience.
> - **Why:** The Echo emerges when all three stims fire simultaneously and integrate. Without that, you're getting flashes of it instead of full versions.

### 7C. MECHANISM EXPLANATION (universal — same for all)

> ### How three stimulations deliver five pleasures
>
> Roughly 80% of women need clitoral stimulation to reach a full peak. Roughly 99% of intimate devices stimulate one zone at a time.
>
> Elysia is built around three coordinated stimulation patterns running together, not in sequence:
>
> - **Pulses** on the surface → delivers **The Strike**
> - **Back-and-forth motion** internally → delivers **The Tide**
> - **Enveloping vibration** across the body → delivers **The Hum**
>
> When all three fire at once, two more pleasures emerge that one-zone devices physically cannot produce:
>
> - **The Slow Burn** — when low-intensity multi-zone stim activates the parasympathetic system instead of the sympathetic one
> - **The Echo** — when the integrated multi-zone climax produces a fully integrated nervous-system afterglow
>
> One zone gives you one or two pleasures. Three coordinated zones give you all five.

### 7D. BUNDLE RECOMMENDATIONS

**The Spark** ($99.99 AUD, was $194.99, save $95) — Recommended for **Strike-dominant** and **Tide-dominant** profiles.
- *Why for these profiles:* Strike and Tide both respond to direct mechanical stimulation. The single device delivers all three coordinated stims, which is sufficient to unlock the missing pleasures.
- Includes: Elysia 3-in-1 device + Discreet Drawstring Pouch + 3 guided rituals.
- Plain packaging, generic bank statement, 30-day full refund even after opening.

**The Wildfire ★ MOST POPULAR** ($129.99 AUD, was $229.99, save $100) — Recommended for **Slow Burn-dominant**, **Hum-dominant**, **Echo-dominant** profiles.
- *Why for these profiles:* These three pleasures depend on parasympathetic activation. The Wildfire bundle adds Ylang-Ylang oil (linalool + geraniol) that drops cortisol — without that, the device's potential goes unrealised. The kit doubles the perceived sensation in our verbatims (3× sensation reported).
- Includes: Elysia 3-in-1 + Pouch + 30ml Ylang-Ylang Essential Oil + 3 guided rituals.
- Plain packaging, generic bank statement, 30-day full refund even after opening.

---

## 8. SOFT EXIT — 4 ACTIVATION CASES

The soft exit fires INSTEAD of the bundle pitch when one of these conditions is met. Trust-building, not selling.

### 8A. Already there (4–5 of 5 selected in Q-C7)
> Headline: *You're already there.*
>
> Body: *Your map is rare. Most women never identify this many pleasures as distinct. We could try to upsell you something. We won't. What's likely useful for you is staying tuned to your nervous system over the years — that's how people in your map keep what they have.*
>
> Resources: 1 free guide *"Maintaining nervous-system response over decades"*.

### 8B. Relational (block = "what my partner would think" + low matter score + Path D/E)
> Headline: *Your map points somewhere a device can't reach.*
>
> Body: *The pattern of your answers points to a connection gap, not a physiological one. A 3-in-1 device addresses the body. It doesn't address what's between two people. We'd rather not waste your money or your trust.*
>
> Resources: 3 free worksheets *(The Honest Conversation / What to Hand Your Doctor / Distinguishing Physiological from Relational Drift)*.

### 8C. Path A 18–22 with very low body literacy (no answer in Q-C7 + low Q-A4 score)
> Headline: *You're at the very start. The full Elysia isn't the right first step.*
>
> Body: *Your map shows you haven't yet identified any of the 5 pleasures as distinct in your own experience. That's not a deficit — it's a starting point. The right first step is body literacy, not a 3-in-1 device.*
>
> Resources: 1 free guide *"The 5 pleasures — explained, with no product"*.

### 8D. Path E 60+ with health red flags (any pain mention OR uncertainty about safety)
> Headline: *Before any device, please speak with a women's health practitioner.*
>
> Body: *Some of your answers suggest a conversation with a women's health practitioner is the right first step before any intimate device. We won't recommend Elysia until you've had that conversation — your safety matters more than our sale.*
>
> Resources: AU women's health practitioner directory (Jean Hailes, Australasian Menopause Society).

---

## 9. TESTIMONIALS — 5 (one per profile, age-anchored to most likely path)

> ⚠️ All testimonials are paid models; quotes are anonymised verbatim composites from the 459-respondent survey. Disclosed in footer.

**Strike profile (Path A or B most likely):**
> *"I always assumed the sharp peak was 'it'. Then I read this and realised I'd been having one fifth of what was possible. Three weeks in, I get what they meant."*
> — **Lisa**, 31, Sydney

**Slow Burn profile (Path B or C most likely):**
> *"I'd been calling it 'the build'. The map called it the Slow Burn and named what was missing after it. Now I know what to expect — and what I'd been settling for."*
> — **Sienna**, 38, Melbourne

**Tide profile (Path C most likely):**
> *"I knew I was 'internal' but I didn't know that was a kind. The map gave me the language. Three weeks in, I had the wave I'd been describing for years."*
> — **Helen**, 49, Brisbane

**Hum profile (Path D most likely):**
> *"My GP said it was normal. I nodded. I went home. Five years later, this map called it the Hum. And then it gave me the device. Karen. I cried."*
> — **Margaret**, 58, Adelaide

**Echo profile (Path E most likely):**
> *"At 64 I'd stopped imagining. The map told me I'd been having Echo-only experiences and what was missing. The kit changed it in two weeks. I'm not done yet."*
> — **Karen**, 64, Perth

---

## 10. ANIMATION DECISION (PENDING)

Previous animations rejected by Alpha:
- Topo map (parchment + contours) — "I don't understand what's happening"
- Sun rising (sky / horizon) — "looks like a bug"

Current state: no animation. Hero is centred vertically with a small gold ornament under CTA.

**Possible options for the questions stage** (decide later):
- Subtle 5-bar visual that fills in as common Q1–Q8 are answered, each bar = one of the 5 pleasures.
- Single soft pulsing dot that intensifies as the map completes.
- No animation — minimal, premium, distraction-free.

**Recommend:** the 5-bar visual — it directly visualises the Big Idea (5 kinds, your scores). Decision deferred until verdict design is finalised.

---

## 11. WHAT THIS FILE IS NOT

- Not the final code. The code happens after audit + Alpha sign-off.
- Not exhaustive verdicts (5 paths × 5 profiles = 25 verdicts assembled at runtime via age opener × profile narrative + universal mechanism + bundle reco).
- Not the analytics events. To be added at code time.
- Not the legal disclaimer. The existing disclaimer in the index.html stays (paid models, verbatim composites, no medical claims).

---

## 12. AUDIT TARGETS — 6 SUB-AGENTS

After Alpha validates this brief, 6 audits run in parallel:

1. **Persona-fit auditor** — does each path × profile combination feel like a real woman would recognise herself? Verbatim consistency check.
2. **Sex-positive ethics auditor** — zero shaming, zero condescension, zero medicalisation of normal variation, zero "broken" framing.
3. **Mechanism cohérence auditor** — are the 5 pleasures defensible physiologically? Is the mapping to 3 stims medically/anatomically accurate? Anti-overclaim check.
4. **Conversion CRO auditor** — completion rate forecast, hero hook strength, time-to-CTA, friction audit.
5. **TGA-AU compliance auditor** — Therapeutic Goods Administration regulations Australia. No therapeutic claim outside scope. Discretionary product positioning.
6. **Age-conditional flow auditor** — does each path A/B/C/D/E feel authentic to its decade, vocabulary-appropriate, no jarring crossover, no missing real-life concern?

Output of each audit: short report (PASS / NEEDS REVISION / CRITICAL) + specific revisions.

Iteration loop until consensus, then code.

---

*Brief prepared 2026-05-07. Ready for Alpha review + 6-agent audit on his go.*
