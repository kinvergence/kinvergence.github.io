# kinvergence.github.io

The Kinvergence front door: <https://kinvergence.github.io/>

**This is an invitation site, not a framework site.** Its job is to make a personal invitation
credible and easy to act on — it is the thing a member sends *after* a conversation, not something
that acquires strangers. It is deliberately much smaller than the written material would support.

The framework itself lives in [kinvergence-core](https://github.com/kinvergence/kinvergence-core):

- [What Kinvergence is](https://github.com/kinvergence/kinvergence-core/blob/main/docs/kinvergence.md), in one sitting
- [The vision](https://github.com/kinvergence/kinvergence-core/blob/main/docs/vision.md) — a proposal, not a settled direction
- [The roadmap](https://github.com/kinvergence/kinvergence-core/blob/main/ROADMAP.md) — § 3a covers this site's scope and the reasoning behind it

## Technical

A single `index.html`. No build step, no dependencies, no external requests, no analytics. Marks are
inlined as SVG; the favicon is an inlined data URI. Open the file in a browser to work on it.

See [DEVELOPMENT.md](DEVELOPMENT.md) before changing the copy — several things in it are
load-bearing and are easy to undo by accident.
