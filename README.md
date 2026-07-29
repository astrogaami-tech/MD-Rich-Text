# MD ⇄ Rich Text

A single-file, browser-based **two-way converter** between Markdown and rich text.
Write Markdown and watch it render live, or paste formatted content from Word, Notion,
or Google Docs and get clean, portable Markdown back.

No installation, no server, no account, no data leaves your machine. Open the HTML file and it runs.

---

## Why this tool exists

Moving text between Markdown-based tools and rich-text apps is usually lossy and annoying —
pasted content arrives full of junk styling, and hand-converting formatting wastes time.
This tool makes the round-trip clean and instant, with a few touches that make it a real
writing surface rather than a throwaway converter:

1. **Both directions in one place.** Markdown → Rich Text *and* Rich Text → Markdown, toggled
   with one click. Draft in Markdown for a live preview, or strip any pasted rich content down
   to portable Markdown.
2. **Live, line-accurate editing.** The preview updates as you type, scrolling stays in sync
   both ways, and **clicking any element in the preview jumps the editor to that exact source
   line** — handy for long documents.
3. **Distraction-free when you want it.** Split, Focus (editor only), and Preview-only layouts,
   plus a draggable divider you can resize or double-click to reset to 50/50.
4. **Clean output you can actually use.** Copy as rich text (pastes with formatting into email,
   docs, etc.), copy as Markdown, **print the preview to PDF** with no UI chrome, or **export a
   standalone styled HTML file**.
5. **Zero footprint.** One HTML file, everything runs locally in the browser.

---

## Features

- **MD → Rich Text** mode: a Markdown editor on the left, a live rendered preview on the right.
- **Rich Text → MD** mode: a paste-here editable area on the left, clean Markdown output on the right.
- **Live preview** with GitHub-flavoured Markdown (tables, code blocks, strikethrough, task-friendly lists).
- **Bidirectional scroll sync** between editor and preview.
- **Click-to-sync** — click a heading, paragraph, list, table, quote, or code block in the
  preview and the editor scrolls to and flashes that line.
- **In-preview anchor links** — heading links (`#section`) scroll within the preview; external
  links open in a new tab.
- **Three layouts** — Split, Focus, Preview — plus divider drag / nudge (◀ ▶) / double-click reset.
- **Live word count.**
- **Export options:**
  - **📋 Copy Rich Text** (formatted HTML to clipboard) / **📋 Copy Markdown** (in RT→MD mode)
  - **🖨 Print PDF** — prints only the rendered preview
  - **⬇ Export HTML** — downloads a clean, self-styled `.html` file (filename auto-slugged from the first heading)
- **✨ Example** loader and **🗑 Clear** button.

---

## How to use it

1. **Open** `MD_Rich_Text_Pro-v1b.html` in a modern browser (Chrome, Edge, or Safari recommended
   for full clipboard support).
2. Pick a direction with the top toggle:
   - **MD → Rich Text:** type or paste Markdown on the left; the styled preview appears on the right.
   - **Rich Text → MD:** paste formatted content (Word / Notion / Google Docs / web) on the left;
     clean Markdown appears on the right.
3. Choose a **layout** — Split, Focus, or Preview — and drag the centre divider to taste
   (double-click it to reset to 50/50).
4. In MD → Rich Text mode, **click any preview block** to jump the editor to its source line.
5. **Get your output:**
   - **Copy** — rich text or Markdown, depending on mode.
   - **Print PDF** — clean preview only.
   - **Export HTML** — a portable, styled standalone file.
6. Use **✨ Example** to load sample content, or **🗑 Clear** to start fresh.

> **Tip:** To clean up messy pasted formatting, switch to **Rich Text → MD**, paste, and copy the
> Markdown — or switch back and re-copy as rich text for a normalised, junk-free version.

---

## Tech & privacy

- **One HTML file.** No framework, no build step.
- **Two small libraries loaded from CDN:**
  [`marked`](https://github.com/markedjs/marked) (Markdown → HTML) and
  [`turndown`](https://github.com/mixmark-io/turndown) (HTML → Markdown).
- **Everything runs in the browser.** Your text is never uploaded anywhere.
- **No persistence.** Nothing is saved between sessions — copy, print, or export anything you
  want to keep. (Because the two libraries load from a CDN, the tool needs an internet
  connection the first time it loads; you can vendor them locally for fully offline use.)
- Rich-text copy uses the async Clipboard API (`text/html` + `text/plain`), which is best
  supported in Chromium browsers and Safari.

---

## License

Released under the **MIT License** — see [LICENSE](LICENSE).

## Credits

Built and maintained by **Astrogaami**.
Powered by the open-source [marked](https://github.com/markedjs/marked) and
[turndown](https://github.com/mixmark-io/turndown) libraries.
