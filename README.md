# Boniface Etim — Writing Portfolio

A single-page static site (`index.html`, no build step).

## Add a video
Open `index.html`, find the `VIDEOS` list near the bottom, and add a line:

```js
{ title: "Video title", tag: "Teaser", description: "Optional one-liner.", url: "https://streamable.com/xxxxxx" },
```

Streamable, YouTube and Vimeo share links are converted to embeds automatically.

## Deploy on Cloudflare Pages
1. Push this folder to a GitHub repo.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git.
3. Build command: leave empty. Output directory: `/` (leave blank).
4. Every push to `main` redeploys automatically.
