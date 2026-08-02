# desh>_

Source for [joindesh.in](https://joindesh.in).

DESH stands for Democratically Elected System Hackers. It is a lab building a
software-defined political party: people who run the systems a country depends
on, applying engineering discipline to governing. India is the first test bed,
and nothing in the design depends on India.

The argument the site is built around is in
[the founding essay](_posts/2025-01-20-corruption-is-gravity.md).

## Running it locally

Jekyll, deployed by GitHub Pages.

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

## Layout

```
index.md          Homepage: the thesis, the engineering, the primitives
about.md          What the lab is
vision.md         What a software-defined state looks like
curriculum.md     The core reading required before contributing
join.md           Who we are looking for and how to apply
primitives.md     Amplifier, Pulse, FlowVote — protocol overviews
_posts/           Writing
_layouts/         default.html, post.html
assets/css/       desh.css — the whole design system, one file
assets/documents/ Litepapers (PDF)
assets/brand/     HTML templates the social images are rendered from
```

## Design

Dark palette on `#07080b`, violet and cyan for the cold half of the metaphor,
ember for thrust. Space Grotesk for display, Inter for body, JetBrains Mono for
the terminal marks. All of it lives in CSS custom properties at the top of
`assets/css/desh.css`.

## Writing

Two rules, and they are the reason the site reads the way it does.

Every claim carries a mechanism or a source. No invented figures, no illustrative
percentages, no code samples that do not run — if a number appears, it is real and
attributable.

Every argument states its own strongest objection. A piece that cannot name where
it is wrong is not finished.

## Contact

help.me@joindesh.in

---

**© 2025 desh>_** · Not left. Not right. Forward.
