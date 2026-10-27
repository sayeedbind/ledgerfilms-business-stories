---
name: ledgerfilms-trend-research
description: Find a real, currently-hot LedgerFilms topic from live signals — Google Trends, YouTube search/trending, Reddit, business news and earnings/announcement calendars — score it against the channel's pillars, and build the keyword & hashtag pack for every publishing platform. Use whenever a LedgerFilms run starts with Topic = Trending (or no topic), whenever the user asks what's hot / what to make next, before a Full-week slate is locked, and again at upload time for titles, tags, hashtags and search keywords. Never invent a topic from memory when this skill can check live signals first.
---

# LedgerFilms Trend Research

The channel does not guess topics. This skill picks them from **dated, linked, live
evidence** of what business & money audiences are searching, watching and arguing about
**right now**, then turns the winning topic into the exact words viewers search for —
so the title, description, tags and hashtags are built from the same research, not
added as an afterthought.

Two jobs, in order:

1. **At the start of a run** — produce a ranked hot-topic slate and a marked pick.
2. **At upload time** — produce the keyword & hashtag pack for the finished video.

The full production rules still live in `../../PLAYBOOK.md`. This skill feeds its §1
intake and §10 handoff; it never replaces the §2 two-source fact-check. **A trend signal
proves people are interested. It never proves a fact.**

## When this skill runs

- Topic is `Trending`, blank, or the user asks "what's hot / what should I make next".
- Mode is **Full week** — run it once, before the week's slate is locked.
- The user gave a topic — run the **light pass** only (§4): check timeliness and search
  phrasing for that topic. Do **not** swap in a trendier topic on your own; if the
  evidence says the user's topic is cold or already saturated, say so once, with the
  numbers, and let the user decide.
- Upload time, for every video — the keyword & hashtag pack (§5) is part of the
  §10 handoff, trend topic or not.

## The workflow

### 1. Scan the sources (in the browser, dated)

Work through `references/sources-and-signals.md` — at minimum **Google Trends,
YouTube, Reddit and one news source** per scan. For every candidate record: the signal,
the source link, the date/timeframe, the geography (default US, then UK/CA/AU), and
whether it is **rising** or merely **big**. Big and flat loses to smaller and rising.
A scan older than 7 days is stale — redo it.

### 2. Filter to the niche

Keep only candidates that fit a LedgerFilms pillar — Rise & Fall · How They Make
Money · Founder Wars · Collapses & Scams · Money Mechanics — and that hide a
**mechanism** a documentary can reveal (how the money actually moves). Drop:
celebrity gossip, sports/entertainment trends, partisan politics, medical claims,
get-rich-quick and price-prediction bait, and anything whose only source is a rumour
or a single social post. See the drop list in `references/sources-and-signals.md`.

### 3. Score and pick

Score every survivor with `references/hot-topic-scoring.md` (trend velocity, search
demand vs. supply, pillar fit, mechanism strength, advertiser fit, evergreen tail,
visual feasibility in VideoExpress, legal risk). Deliver a slate of **up to 5** in a
`templates/trend-brief.md`: each with its evidence links, its "why now", its publish-by
window, and its score. **Mark one pick (★)** and say in one line why it wins. Then
proceed with the pick — the user can redirect to any other slate item.

### 4. Light pass (user supplied the topic)

Skip the slate. Check: is anything making this topic timely *this week* (earnings,
anniversary, news hook, a spike in Trends/YouTube search)? Which exact phrases are
viewers searching (autocomplete + Trends related queries)? Return those two things and
continue into PLAYBOOK §2 research as normal.

### 5. Keyword & hashtag pack (upload time)

Follow `references/keywords-and-hashtags.md`. Build it from the *same* evidence as
the topic scan — autocomplete phrases, Trends related queries, the words Reddit and
YouTube commenters actually use — never from generic SEO lists. Fill the keyword /
hashtag section of `templates/upload-metadata.md` for: **YouTube long-form, YouTube
Shorts, TikTok, Instagram Reels, Facebook, and X**. One primary keyword per video;
every other keyword must be a phrase a viewer would actually type.

## Hard rules

1. **Live or it didn't happen.** Every trend claim in the brief carries a source link
   and a date. No link + no date = not a signal, it's a guess — label it that way.
2. **Interest ≠ truth.** Trend sources are never fact sources. Every load-bearing
   fact from the winning topic still goes through PLAYBOOK §2 (two sources, one
   primary where possible) before a word of script is written.
3. **No hype-chasing off-niche.** A trend that doesn't fit a pillar is not a topic,
   however hot it is. The pillars are the channel.
4. **No financial advice, ever** — not in a topic, a title, a keyword or a hashtag.
   No "buy", "will crash", price targets or return promises, even if that's the
   phrasing that's trending. Rephrase to the mechanism.
5. **Legal ladder applies at topic stage.** A trending accusation against a living
   person or active company is not a topic until a court, regulator or major outlet
   backs it (PLAYBOOK §2, `../../docs/fact-check-and-legal.md`).
6. **Freshness windows are real.** If the pick's window is 48 hours and production
   takes a week, say so and pick the candidate whose window fits the cadence
   (1 long-form + 4 Shorts, work one week ahead) — or make it a Short first.
7. **Don't copy competitors.** Other channels' titles and tags are demand evidence,
   not text to reuse. Titles and hashtags are written fresh from the phrases found.
