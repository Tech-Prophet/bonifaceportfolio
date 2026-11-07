# Boniface Etim — Writing Portfolio

A single-page static site (`index.html`, no build step).

## Add a video
Open `public/index.html`, find the `VIDEOS` list near the bottom, and add a line:

```js
{ title: "Video title", tag: "Teaser", description: "Optional one-liner.", url: "https://streamable.com/xxxxxx" },
```

Streamable, YouTube and Vimeo share links are converted to embeds automatically.

## Connect the contact form
1. Create a free form at https://formspree.io (it emails messages to you, so your address never shows on the site).
2. Copy the form URL (looks like `https://formspree.io/f/xxxxxxxx`).
3. In `public/index.html`, paste it into `const CONTACT_FORM_ENDPOINT = "";`.

## Deploy on Cloudflare (Workers & Pages)
The site is static: `public/index.html` is served as-is, configured by `wrangler.jsonc`.
1. Push this repo to GitHub.
2. Cloudflare dashboard → Workers & Pages → Create → Import a repository.
3. Project name: `bonifaceportfolio` (must match `name` in `wrangler.jsonc`).
4. Build command: leave empty. Deploy command: `npx wrangler deploy`.
5. Every push to `main` redeploys automatically.
