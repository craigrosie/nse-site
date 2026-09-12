# Nonsuch Estate planning applications

A single-page information site about the planning applications at Nonsuch Estate,
published with GitHub Pages from the root of the `main` branch.

## Viewing the site locally

From the repository root:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

Use the server rather than opening `index.html` directly — it serves the same
relative paths GitHub Pages does, so broken links show up locally instead of after
a deploy.

## Editing the content

Everything lives in two files:

- `index.html` — all the text and structure
- `style.css` — all the styling

There is no build step. Commit to `main` and GitHub Pages redeploys within a minute
or two.

## The comment deadline

The deadline appears in three places:

- the `DEADLINE` constant in the countdown script at the bottom of `index.html`
- the static fallback text in the elements marked `data-countdown` (shown when
  JavaScript is unavailable)
- the prose: the bar at the top of the page and the "Comments close on…" heading

Change all of them together.

## Placeholders

All of the original bracketed placeholders have been filled in. The only bracketed
uppercase text remaining in `index.html` is `[PLANNING REF]` in the "By email"
section, which is deliberate — it's part of the example subject line, not a TODO.

There is no local detail yet on which route these applications are expected to
take (delegated decision vs. planning committee) — that was previously an
unanswered FAQ, which was removed rather than left with a guess. Add it back as an
FAQ entry if and when that becomes known.

To check for any new placeholders after editing:

```bash
grep -o '\[[A-Z0-9][^]]*\]' index.html | sort -u
```
