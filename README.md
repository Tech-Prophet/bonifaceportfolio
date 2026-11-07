# Boniface Etim — Writing Portfolio

A single-page static site (`index.html`, no build step).

## Add a video
Open `index.html`, find the `VIDEOS` list near the bottom, and add a line:

```js
{ title: "Video title", tag: "Teaser", description: "Optional one-liner.", url: "https://streamable.com/xxxxxx" },
```

Streamable, YouTube and Vimeo share links are converted to embeds automatically.

## Connect the contact form
1. Create a free form at https://formspree.io (it emails messages to you, so your address never shows on the site).
2. Copy the form URL (looks like `https://formspree.io/f/xxxxxxxx`).
3. In `index.html`, paste it into `const CONTACT_FORM_ENDPOINT = "";`.

## Deploy on Cloudflare Pages
1. Push this folder to a GitHub repo.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git.
3. Build command: leave empty. Output directory: `/` (leave blank).
4. Every push to `main` redeploys automatically.
