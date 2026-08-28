# kinvergence.github.io

The Kinvergence front door: <https://kinvergence.org> (also served at
<https://kinvergence.github.io/>).

**This is an invitation site, not a framework site.** Its job is to make a personal invitation
credible and easy to act on — it is the thing a member sends *after* a conversation, not something
that acquires strangers. It is deliberately much smaller than the written material would support.

**This site is also the publication.** `kinvergence-core` is a private working corpus, not a
destination for readers; material is curated and rewritten onto these pages rather than linked to in
place. Do not add links into that repository. The reasoning is in
[DEVELOPMENT.md](DEVELOPMENT.md) § The repository is not the publication.

## Pages

| File | What it is |
|---|---|
| `index.html` | The invitation. Four short sections, each opening onto one of the pages below |
| `story.html` | How the first family's practice actually formed, with dates and quotations |
| `heartbeat.html` | How to run the weekly meeting, and what comes after it |
| `honesty.html` | What we have never tested, what would prove us wrong, and who holds this |

## Technical

Static HTML. No build step, no dependencies, no external requests, no analytics. Shared styles in
`assets/site.css` and the nav script in `assets/site.js`; everything else — the nav markup, the
footer, the inlined SVG marks and favicon — is duplicated per page on purpose, because there is no
templating layer and there does not need to be one at four pages. **If you change the nav or the
footer, change it in all four.**

Open any file in a browser to work on it.

See [DEVELOPMENT.md](DEVELOPMENT.md) before changing the copy — several things in it are
load-bearing and are easy to undo by accident.
