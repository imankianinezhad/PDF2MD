# PDF to Markdown Converter

A single-file, browser-based PDF → Markdown converter for **English, Français and فارسی (Persian)**.
Everything runs locally in the browser: your files are never uploaded to a server.

Developed by [imankiani.com](https://imankiani.com/).

## Features

- Upload a PDF (drag & drop or file picker) or load one from a URL
- Detects headings, bold/italic, bulleted and numbered lists, tables and multi-column pages
- Removes repeated headers/footers and joins hyphenated words
- Right-to-left support for Persian/Arabic, including mixed Persian + Latin text; ZWNJ is preserved
- Optional Persian/Arabic character and digit normalization
- Editable output, live preview, copy to clipboard and save as `.md`
- Responsive UI for desktop and mobile, automatic light/dark theme

## Run locally

Just open `index.html` in a browser. Or serve the folder:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Deploy on GitHub Pages

1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`.
4. Your site will be available at `https://<username>.github.io/<repo>/`.

## Notes and limitations

- **URL loading** only works when the remote server allows cross-origin requests (CORS). Otherwise download the PDF and upload it.
- **Scanned PDFs** (images without a text layer) need OCR, which is not included.
- Images and math formulas inside the PDF are not extracted.
- Libraries are loaded from CDNs: [pdf.js](https://mozilla.github.io/pdf.js/) 3.11.174 and [marked](https://marked.js.org/) 4.3.0 (cdnjs), and fonts from Google Fonts. To work fully offline, download these files and update the `<script>` / `<link>` tags in `index.html`.

## License

MIT
