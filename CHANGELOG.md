---
maintenance_instructions: |
  Dated history of the site's build (Pass 1, Pass 2, feedback received and applied, decisions
  reached), in the spirit of Keep a Changelog — no semver, since this site doesn't ship versioned
  releases. Newest entries first. This is where DEVELOPMENT.md content lands the moment it
  resolves or turns into narrative — add an entry in the same edit that trims DEVELOPMENT.md,
  never let DEVELOPMENT.md accumulate a history or a feedback-awaiting-action table waiting to be
  moved here.
---

# Changelog

Dated history of the site — what changed, why, and feedback received. `DEVELOPMENT.md` stays
current-state only; this file is where its history lands.

## 2026-08-27 — Julia's Pass 2 feedback received

Received via the SFV Telegram group the night of 2026-08-27 — Julia's first read of the four-page
site. She validated the four-page split ("like a quick start option when you buy a new tool"), the
timeline ("so, so cool," "leaving no trace... so important"), the honesty page's errors section
("illuminating... people will like seeing that"), and the reversal of her Pass 1 "AI slop" reaction.
The load-bearing honest limit landed as intended ("This sums up the purpose of the site succinctly
and clearly"). Sign-off: *"Well done, Little Brother. I like this direction."*

Two items flagged actionable, **not yet applied as of this writing** — revisit before Julia's 09-18
reunion and before treating Pass 2 as done:

1. "Carried in the open…" under "What we do not know" read as ambiguous even to a sympathetic reader
   — needs a clearer rephrase on `honesty.html`.
2. The "Put it on the calendar" ask barely registered ("did not jump out... perhaps it was the blue
   color") — the most important item, since the ask is the whole point of the site. This tensions
   with the 2026-08-27 ask-color decision below (changed to navy for a *different* reason, avoiding
   near-black), so under-visibility here may be a weight/whitespace problem rather than a hue one —
   needs a fresh look at the section as a whole, not just another color swap.

## 2026-08-27 — Pass 2: three curated pages, and the home page finally gets short

Split into four pages with shared `assets/site.css` and `assets/site.js`. The home page went
1,710 → ~1,170 words, 41% below the 2026-08-25 original, which Pass 1's sentence-level editing could
not achieve on its own. The structural point: Ed's *"there should be deeper content"* and Julia's
*"way too wordy"* looked like opposite instructions and were the same one — move depth off the front
page. Nothing was deleted; the front page got shorter and the site got deeper in the same operation.

`story.html` and `honesty.html` gained material the site had never shown a reader before: corrections
to the family's own published history, and an explicit statement of what would falsify the framework.
The cadence diagram (`index.html` § 3 — three rows over a twelve-column grid, pure CSS, no image) was
added in the same pass, answering a request to show *a little structure* without importing any of the
model's notation.

Also: the 2026-08-25 "honest limits never collapsed, never moved" decision was deliberately reopened
— four of five limits moved to `honesty.html` to get the home page short enough to actually be read.
The guard: the load-bearing limit stays inside the ask at full weight as its own justification, and
the link to `honesty.html` must never become a footnote.

## 2026-08-27 — Pass 1: voice, concision, correctness

Moved the whole page into first person with members named — the single finding worth carrying
forward: Julia's *"way too wordy — sets off my AI slop radar"* and Ed's *"it's a lot of text"* were
the same defect with one cause. The page narrated SFV in the third person while being written by SFV,
and every fact had to be routed through an anonymizing construction; those constructions were the
adjectives. Julia's own proposed fix (*"Ex.: 'This is our family, and we would like to know…'"*) is
now the hero's closing sentence nearly verbatim.

Body copy fell from 1,996 to 1,710 words — 14%, not the third originally aimed for. Two rounds of
cutting produced diminishing returns: what was left was structure, not padding (story 526 words,
practice 442, the ask 337, hopes 297, hero 108). The remaining reduction had to come from moving
content onto separate pages, not editing sentences — which Pass 2 (above) did.

Also fixed: a heading/nav-label mismatch ("What this could be" vs. "What we want this to become," now
unified as "What we hope this becomes"); a false claim about being short of interest rather than a
second family (deleted, not reworded); "Three things that are easy to get wrong" actually listing
four; the founding blockquote overflowing `.measure`; `-webkit-backdrop-filter` added for Safari/iOS.
Seven GitHub links into `kinvergence-core` were removed. Added from the 2026-08-26/27 timeline
revisions: Derek's *"I hate meetings. but I look forward to FV meetings…"*; the first Demo Day being a
week late (Derek was sick); the annual themes; and the cadence claim rephrased as "the longest we ever
went without a Heartbeat was three weeks" to respect the no-cumulative-counts rule.

**Decisions settled in this pass:** ask section changed to deep navy (`--slate-deep`), not
near-black, on Julia's reaction. Member naming settled — yes, first names only, decided 2026-08-27;
the credibility gain and anti-"AI slop" effect were larger than expected, and the privacy cost small
since all four are already public on the SFV site.

## 2026-08-25 — Site built

Single page, four sections, verified at 375px/768px/1440px. Nothing about the page's factual claims
has needed changing since, including through the 2026-08-26 timeline corrections — a consequence of
the no-cumulative-counts rule rather than luck.
