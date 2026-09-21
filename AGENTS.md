# timeline

A standalone, static timeline component: `timeline.html` (71 lines) and
`stylesheet.css` (163 lines). No build step, no package manager, no tests, no
dependencies to install. Open `timeline.html` in a browser and that is the whole
development loop.

This is an old demo kept for reference. Treat changes as conservative maintenance
rather than modernization, unless asked otherwise.

## TODO

- [#2](https://github.com/castastrophe/timeline/issues/2): the inline hover handler
  calls jQuery, which the page never loads, so the interaction has never worked.
  Decide there before touching the JS.

## Structure

`.timeline` wraps a list of `.timeline-item` elements. The interaction toggles
`.active` on the hovered item and `.close` on its immediate siblings; the CSS does the
rest. Any new markup needs to keep that three-class contract.

Never add AI attribution to a commit or a PR: no `Co-Authored-By` trailer, no
"Generated with …" footer, no session URLs.

## Prose style

Prose in this repo (README, commit bodies, PR descriptions) follows the
[style guide](https://github.com/castastrophe/.github/blob/main/AGENTS.md#style-guide):
sentence-case headings, `&` over "and", `:` over em dashes.
