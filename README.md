# [SITE NAME] planning applications

A single-page information site about the planning applications at [SITE NAME],
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

## Placeholders to fill in

Every item below appears in `index.html` as bracketed uppercase text. Search for the
token and replace it, including the square brackets.

- [ ] `[INTRO PARAGRAPH]` — what is now proposed, where, and roughly how large.
- [ ] `[SITE PLAN IMAGE]` — export a page of the Proposed Site Layout PDF as an image,
      save it under `images/`, and swap the `.site-plan__placeholder` div for the
      commented-out `<img class="plate">` next to it. Give the image a real `alt`.
- [ ] `[APPLICATION 1 DESCRIPTION]` — one plain-English sentence.
- [ ] `[APPLICATION 2 DESCRIPTION]` — one plain-English sentence.
- [ ] `[KEY DOCUMENTS]` — the two or three documents most worth reading, with links.
- [ ] `[OBJECTION 1 HEADING]` and `[OBJECTION 1 BODY]`
- [ ] `[OBJECTION 2 HEADING]` and `[OBJECTION 2 BODY]`
- [ ] `[OBJECTION 3 HEADING]` and `[OBJECTION 3 BODY]`
- [ ] `[OBJECTION 4 HEADING]` and `[OBJECTION 4 BODY]`
- [ ] `[TODO: when to pick this]` — appears twice, for Neighbour and Member of the
      Public under **Commentator Type**.
- [ ] `[CALLOUT ABOUT CLICKING NEXT]` — what the confirmation looks like, so people
      know their comment went through.
- [ ] `[ADD: local detail…]` — in the "What happens after comments close?" answer,
      which route these applications are expected to take.
- [ ] `[EMAIL ADDRESS]` — appears twice, once as link text and once in the `mailto:`.
- [ ] `[LAST UPDATED DATE]` — in the footer.
- [ ] `[WHO RUNS THIS SITE]` — in the footer.

`[PLANNING REF]` in the "By email" section is deliberate — it is part of the example
subject line, not a placeholder.

To find any that remain:

```bash
grep -o '\[[A-Z0-9][^]]*\]' index.html | sort -u
```
