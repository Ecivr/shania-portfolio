# Shania Samantha Jackline: portfolio

One file (`index.html`), no build step. Her photo is embedded inside it, so there is nothing else to upload.

## Free hosting (pick one)
**GitHub Pages**
1. Create a free GitHub account and a new public repository (e.g. `shania-portfolio`).
2. Upload `index.html`.
3. Settings, Pages, Source: "Deploy from a branch", branch `main`, folder `/ (root)`, Save.
4. The link appears as `https://USERNAME.github.io/shania-portfolio/` within a minute or two.

**Netlify Drop**: go to app.netlify.com/drop, drag the folder in, then rename the site under Site settings.

**Cloudflare Pages**: Workers & Pages, Create, Pages, Upload assets, drop in the folder.

## Updating the contact links
Email and LinkedIn are set in the contact section at the bottom of `index.html` (search for `mailto:` and `linkedin.com/in/`). After any edit, upload the file again and the live link updates.

## Changing the photo later
The photo is stored inside `index.html` as base64 text. To swap it, make a square, face-centered image (at least 800 x 800 px for sharp results on phones), then run:

    python3 -c "import base64;print(base64.b64encode(open('photo.jpg','rb').read()).decode())"

Copy the output and paste it over the long text after `data:image/jpeg;base64,` in the `<img>` tag inside the `arch` div. Keep the JPEG under about 150 KB so the page stays fast.

## Notes
- Fonts load from Google Fonts; the page still works offline with fallback fonts.
- Dark mode and reduced-motion preferences are respected automatically.
