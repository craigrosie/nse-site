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

## Placeholders to fill in

Every item below appears in `index.html` as bracketed uppercase text. Search for the
token and replace it, including the square brackets.

- [ ] `[SITE NAME]` — the name of the site or development. Appears in the page title,
      the meta description, and the `<h1>`.
- [ ] `[ONE LINE SUMMARY OF WHAT IS PROPOSED]` — the subtitle under the main heading.
- [ ] `[INTRO PARAGRAPH]` — what is proposed, where, and roughly how large.
- [ ] `[SECOND INTRO SENTENCE]` — why it matters to people living nearby.
- [ ] `[COUNCIL NAME]` — the local planning authority. Appears twice.
- [ ] `[DEADLINE DATE]` — the date comments close. Appears twice: in the top callout
      and in the callout at the end of the page. Both must be updated.
- [ ] `[COMMENT FORM URL]` — where the "Comment on the applications" buttons point.
      Appears twice.
- [ ] `[APPLICATION 1 REF]` — the first application's reference number. Appears twice.
- [ ] `[APPLICATION 1 DESCRIPTION]` — one plain-English sentence.
- [ ] `[APPLICATION 1 PORTAL URL]` — the council portal page for application 1.
- [ ] `[APPLICATION 2 REF]` — the second application's reference number. Appears twice.
- [ ] `[APPLICATION 2 DESCRIPTION]` — one plain-English sentence.
- [ ] `[APPLICATION 2 PORTAL URL]` — the council portal page for application 2.
- [ ] `[OBJECTION 1 HEADING]` and `[OBJECTION 1 BODY]`
- [ ] `[OBJECTION 2 HEADING]` and `[OBJECTION 2 BODY]`
- [ ] `[OBJECTION 3 HEADING]` and `[OBJECTION 3 BODY]`
- [ ] `[OBJECTION 4 HEADING]` and `[OBJECTION 4 BODY]`
- [ ] `[COUNCIL EMAIL]` — appears twice, once as link text and once in the `mailto:`.
- [ ] `[COUNCIL POSTAL ADDRESS]`
- [ ] `[LAST UPDATED DATE]` — in the footer.
- [ ] `[WHO RUNS THIS SITE]` — in the footer.

To find any that remain:

```bash
grep -o '\[[A-Z0-9 ]*\]' index.html | sort -u
```
