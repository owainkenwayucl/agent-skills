---
name: news-briefing
description: Produce a fresh, personalized news briefing across Steam new releases, Warhammer 40k, BattleTech, AI/HPC, pro wrestling (WWE, AAA, JCW) and a brief US/UK politics note. Use when the user asks for their news rundown, daily/periodic briefing, "what's new", or a roundup across these hobbies.
---

# Personalized news briefing

Produce a short, fresh news briefing for this user. The briefing is hobby-first,
with politics deliberately a small footnote.

## Workflow

1. **Gather fresh items per section** using `web_search`, then `web_fetch` the
   best 1-3 candidate pages to confirm the date and detail. Read
   `references/sources.md` for the preferred sources and suggested queries per
   topic; reuse it rather than inventing sources.

2. **Filter hard for freshness and relevance.** See the rules below.

3. **Write the briefing** using the exact template at the end of this file.

## Freshness and relevance rules

- Default window: **last 48 hours**. Loosen to **last 7 days** only where news
  genuinely moves slower (Black Library / BattleTech novels, tabletop product
  announcements, AAA/JCW shows, major AI papers).
- Every item must carry a date (or clear relative recency) and a source link.
  Drop anything you cannot date.
- **Deduplicate.** One item per story. If a story recurs across sections, put it
  where it fits best and don't repeat it.
- **New Steam releases only:** actual releases or release-date announcements,
  not wishlist/sale/update noise. Prefer notable or well-reviewed releases; skip
  asset flips and shovelware.
- **AI/HPC:** prioritize capability/product/funding/benchmark/hardware and
  supercomputing news. Skip opinion pieces, listicles, and pure hype unless the
  user's interest is clear.
- **Politics (US/UK):** maximum **3 short bullets**, and only genuinely
  significant items (elections, major legislation, big policy/economic news).
  If nothing significant is fresh, write "Nothing notable in the window." Do not
  let this section grow.
- **Wrestling:** prioritize WWE (TV results/angles, PPV build, signings, injury
  and title news), then AAA, then JCW. Keep spoilers to results the user is
  likely to have already seen unless the item is important.
- **Label uncertainty.** Mark rumors, leaks, and unconfirmed reports explicitly
  as such. Never present a rumor as fact.
- If a section has nothing fresh, say so in one line. **Do not pad.**

## Output template

Use this structure every time. Keep the whole briefing roughly 30-50 lines.
Bold headlines, one-sentence summaries, dates and links.

```markdown
# News Briefing — <Weekday DD Mon YYYY, HH:MM TZ>

## 🕹️ Video games — new on Steam
- **<Game>** — <what it is, genre/tag, why it matters> · released <date> · [Steam](<url>)

## ⚔️ Warhammer 40k
- **<Headline>** — <one sentence> · <date> · [source](<url>)

## 🤖 BattleTech
- **<Headline>** — <one sentence> · <date> · [source](<url>)

## 🧠 AI & HPC
- **<Headline>** — <one sentence> · <date> · [source](<url>)

## 🤼 Pro wrestling
- **WWE:** <headline> · <date> · [source](<url>)
- **AAA:** <headline> · <date> · [source](<url>)
- **JCW:** <headline> · <date> · [source](<url>)

## 🏛️ US/UK politics (brief)
- <max 3 bullets, or "Nothing notable in the window.">
```

## Style rules

- Lead with the fact, not the outlet. "**Space Marine 2 gets new season** — ..."
  beats "According to IGN, ...".
- One sentence per bullet, then the date and link. No filler like "In a
  surprising turn of events".
- Use `web_search` `time_range` (`day` or `week`) to bias toward fresh results.
- Cite the source page you actually read. If a search snippet was enough, still
  link the page.
- Flag when you could not verify something rather than silently omitting it.

## Notes / upkeep

- **JCW = Juggalo Championship Wrestling** (confirmed by the user). Report JCW as
  Juggalo Championship Wrestling; do not confuse it with Jersey Championship
  Wrestling. Always spell out the full promotion name at least once per briefing.
- After editing this skill, run `/reload` in Pi and test with
  `/skill:news-briefing`.
