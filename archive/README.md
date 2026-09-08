# Anomaly archive

Open `archive.html` to view the case index. This is a standalone static page; no build or JavaScript is required.

## Add a case

1. Create the case page (for example, `archive/cases/your-case.html`).
2. In `archive.html`, find `<ul class="case-list">`.
3. Copy the commented sample `<li>...</li>` into that list, outside the comment.
4. Replace its `href`, reference, title, and summary. Paths are relative to `archive.html`.

Repeat for each case in the order you want to display them. The empty notice automatically disappears when the list contains a `.case-link`. No case totals or dates need updating. Keep the example commented until a real destination exists, to avoid broken links.
