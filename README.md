# Mr. House — The house always builds

A static blog. No build step, no framework, no trackers — just HTML and one stylesheet.

## Structure

- `index.html` — home page: marquee masthead, essay list ("The Ledger"), about box, footer
- `style.css` — all styling (design tokens are CSS variables at the top)
- `posts/*.html` — one file per essay

## Writing a new post

1. Copy any file in `posts/` and rename it (kebab-case, e.g. `posts/my-new-essay.html`).
2. Update the `<title>`, `<meta name="description">`, the `.meta` line (date · read time · tag), the `<h1>`, and the body paragraphs.
3. Add a matching `<a class="entry">` block at the **top** of "The Ledger" list in `index.html` (newest first).

Tags in use: `Manifesto`, `Life`, `Building` — add whatever fits; it's just text.

## Preview locally

```bash
python3 -m http.server 4173 -d .
```

Then open http://localhost:4173.

## Deploy

Any static host works — drag the folder into Netlify, or:

- **GitHub Pages**: push this folder to a repo, enable Pages on the main branch
- **Vercel**: `vercel .` (no config needed)
- **Cloudflare Pages**: connect the repo, no build command, output dir `/`

Footer links point to [x.com/MrHouse_eth](https://x.com/MrHouse_eth) and [github.com/mrhouse223](https://github.com/mrhouse223). Add a Farcaster link there once the account exists.
