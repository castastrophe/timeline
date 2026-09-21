# timeline

A standalone, static timeline component: `timeline.html` (71 lines) and
`stylesheet.css` (163 lines). No build step, no package manager, no tests, no
dependencies to install. Open `timeline.html` in a browser and that is the whole
development loop.

This is an old demo kept for reference. Treat changes as conservative maintenance
rather than modernization, unless asked otherwise.

## Known issue — read before touching the JS

The inline `<script>` in `timeline.html` uses jQuery (`$(".timeline-item").hover(…)`),
but jQuery is never loaded on the page. The hover interaction has therefore never
worked in this file as committed. Two honest options if it comes up:

1. Rewrite the handler in plain DOM APIs — it's about six lines, and it's what the
   rest of the file's age argues for.
2. Add the jQuery `<script>` tag and keep it as-is.

Either is fine. What isn't fine is quietly "fixing" surrounding code while leaving the
handler dead, which is how it got this far.

## Structure

`.timeline` wraps a list of `.timeline-item` elements. The interaction toggles
`.active` on the hovered item and `.close` on its immediate siblings; the CSS does the
rest. Any new markup needs to keep that three-class contract.

Never add AI attribution to a commit or a PR: no `Co-Authored-By` trailer, no
"Generated with …" footer, no session URLs.
