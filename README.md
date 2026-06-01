# Page Editor → Claude

A zero-install browser bookmarklet that makes **any webpage editable**, tracks your changes at the word level, and copies a clean before/after diff you can paste straight back to Claude.

No extension, no build step, no data leaves your browser. It's a single `javascript:` bookmarklet.

## Install

Open [`index.html`](index.html) (or the published page) and **drag the "✏️ Edit Page" button to your bookmarks bar**.

If your bookmarks bar is hidden, show it with <kbd>Cmd/Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>B</kbd>.

## How it works

1. **Go to any webpage** and click the **Edit Page** bookmark. A toolbar appears at the top and the whole page becomes editable — click any text and start typing.
2. **Edit in place.** The bookmarklet snapshots every text node when it loads, so it knows exactly what changed.
3. **Copy or Review:**
   - **Copy** — grabs every change as structured `ORIGINAL` / `EDITED` pairs.
   - **Review** — opens a panel with word-level diffs (deleted words struck through, added words highlighted green) so you can uncheck anything you want to skip before copying.
4. **Paste into Claude** and tell it what to do — "apply these to the Figma copy," "tighten the tone," "turn these into a changelog," etc.

Edits are local to your browser session — nothing is saved on the actual site. Refresh to reset.

## What gets copied

```
I edited text on <page url>. Here are my changes:

--- ORIGINAL ---
The old sentence.
--- EDITED ---
The new sentence.
```

## Features

- **Instant edit mode** — one click enables `contentEditable` on the entire page.
- **Word-level diffs** — the review panel highlights exactly which words were removed and added.
- **Selective copy** — uncheck individual changes before exporting.
- **Claude-ready output** — structured `ORIGINAL` / `EDITED` pairs, ready to paste.

## Files

- `index.html` — the install/landing page with the draggable bookmarklet and usage steps. The bookmarklet source lives in the `href` of the drag button.

## License

MIT — do whatever you like with it.
