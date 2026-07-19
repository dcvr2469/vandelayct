# Vandelay Construction Technologies — Website

Static site: `index.html`, `styles.css`, and `assets/logo.svg`. No build step, no dependencies beyond Google Fonts (loaded via CDN link in `<head>`).

## Hosting on GitHub Pages

1. Create a new repository (e.g. `vandelayct-site`) and push these three files/folders to the root of the `main` branch:
   - `index.html`
   - `styles.css`
   - `assets/logo.svg`
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/`.
5. If you're pointing the `vandelayct.com` domain at this repo, add a `CNAME` file at the root containing just:
   ```
   vandelayct.com
   ```
   Then set your domain registrar's DNS to point at GitHub Pages (an `A` record set to GitHub's IPs, or a `CNAME` record to `<your-username>.github.io` for a subdomain).

## Notes

- The contact form currently has no backend (`action="#"`) — wire it up to a form service (e.g. Formspree, Netlify Forms) or your own endpoint before it goes live.
- Fonts: Oswald (headings) + Source Sans 3 (body), loaded from Google Fonts.
- Colors and layout are defined as CSS custom properties at the top of `styles.css` if you want to adjust the palette later.
