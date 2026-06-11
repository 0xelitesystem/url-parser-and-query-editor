# URL Parser and Query Editor

Break a URL into its parts, edit the query parameters in a table, and rebuild it live. No server, no tracking, no third-party scripts.

**Live demo:** https://0xelitesystem.github.io/url-parser-and-query-editor/

## Use

Open `index.html` in any modern browser, or visit the GitHub Pages link in the repo description.

Paste a URL and hit Parse (or press Enter). The tool splits it into:

- Protocol, host, port, path, query, and hash

The query parameters land in an editable table. You can:

- Edit any key or value in place
- Add a new parameter row
- Remove a parameter

The rebuilt URL updates as you edit, with values properly percent-encoded, and a copy button puts it on your clipboard. If you paste a bare host like `example.com/path`, the tool assumes `https://` so it still parses.

## Why this exists

Editing query strings by hand is error-prone, and the online tools that do it tend to load tracking scripts and ads. This is the same idea, single file, no analytics, no signup, MIT licensed.

## Privacy

Everything runs in your browser. The URL you paste never leaves your machine. Verify by viewing the page source or by opening DevTools and watching the network tab, no requests are made.

## Run locally

```bash
git clone https://github.com/0xelitesystem/url-parser-and-query-editor
cd url-parser-and-query-editor
# Open index.html in your browser, or:
python -m http.server 8000
```

## Contribute

Issues and PRs welcome:

- Parsing edge cases (userinfo, IPv6 hosts, matrix params)
- Encoding and decoding options
- UI improvements (keep it minimal, no frameworks)
- Translations

Don't add: analytics, tracking, external scripts, npm dependencies. The whole point of this tool is no surveillance.

## Build

There is no build. It's a single HTML file.

## License

MIT.

## Related

- [color-format-converter](https://github.com/0xelitesystem/color-format-converter), convert between HEX, RGB, HSL, and HSV
- [aspect-ratio-calculator](https://github.com/0xelitesystem/aspect-ratio-calculator), simplify dimensions to a ratio and back
- [word-and-character-counter](https://github.com/0xelitesystem/word-and-character-counter), count words, characters, and reading time
