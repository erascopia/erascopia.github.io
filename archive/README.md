# Panic Operator content taxonomy

`/archive.html` is the master index. `/archive/archive.html` forwards to it to preserve the old URL. The homepage is `/index.html`; it and the index share `/assets/site.css`. There is no build step or dependency requirement.

- **Case / case file**: a canonical investigated event with a permanent `FILE ###` identifier.
- **Evidence**: footage, images, timestamps, notes and artifacts belonging to a File.
- **Transmission**: a fragment, sighting or signal that does not consume a File number. Numbered audio transmissions currently use T-001–T-004. Unclassified visual fragments have descriptive names, not canonical numbers.
- **Archive**: the master index of canonical Files. “Record” is prose, not a separate category.

## Publishing a case

1. Add a real case page under `/cases/<number>/` with its evidence and permanent identifier.
2. Add `.case-card` markup to `/archive.html`, newest first. The homepage links to the archive without repeating the index.
3. Update published/open/filed counts on the archive page. A File number is not a count. Currently only FILE 010 has a published destination; do not fabricate Files 001–009.
4. For a new current case, update the hero title, summary, destination, image, social preview metadata together. Evidence stays on the case page. Keep complete paid evidence explicitly labeled.
5. Generate lightweight homepage image derivatives while retaining original case evidence.

## Follow-up data extraction

The current case, card copies, counts, evidence captions/URLs and visual transmission content remain in HTML. Audio metadata and working media URLs are in HTML too; JavaScript only handles menu dismissal, playback coordination and error messages. Move these into separate case and transmission collections with a small static generator if the catalog grows; keep rendered HTML available without JavaScript. Product and social URLs are also maintained in HTML.

Unused old hero/placeholder, archive-entry, network-node, book-callout and reveal selectors have been removed from the shared stylesheet. `main.html` is an older standalone homepage with duplicated inline styles; audit inbound links before retiring it. The case page still has its original standalone inline theme, including unused register selectors that can be removed in a case-template cleanup.
