# Putting hanchen's site on a public address

Nothing here has been bought or signed up for. `index.html` is the whole site; it has no build step.

## Route A: free address, no purchases (about 15 minutes)
1. Create a free GitHub account (or use yours) and a public repository named `<your-username>.github.io`.
2. Upload `index.html`, `404.html` and `robots.txt` from this folder to the repository root.
3. In the repository: Settings > Pages > Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
4. The site is live at `https://<your-username>.github.io`. HTTPS is automatic.

## Route B: your own domain (the only step that costs money)
1. Buy a domain. See the cost table in the launch plan. As a UCLA student, check the GitHub Student Developer Pack first for a free first year.
2. In the repository: Settings > Pages > Custom domain: enter the domain. GitHub creates a `CNAME` file for you.
3. At your registrar, add the DNS records GitHub lists (four A records for the bare domain, one CNAME for `www`).
4. Tick "Enforce HTTPS" once the certificate is issued.
5. Edit `robots.txt` and `sitemap.xml`: replace `YOUR-DOMAIN` with the real one, then upload `sitemap.xml` too.

## Optional, all free
- Email at your domain: Cloudflare Email Routing forwards `hello@your-domain` to your inbox. Requires the domain's DNS to be on Cloudflare.
- Visitor counts: Cloudflare Web Analytics or GoatCounter. One script tag each; not installed.

## Before going public
- Résumé PDF: the "Download PDF" button on the résumé page is switched off. Your current PDF shows your phone number, which you chose to keep off the site. Export a version without it, save it here as `resume.pdf`, then delete the word `hidden` from the line containing `id="pdf-link"` in `index.html`.
- Photo: there is no photo slot yet. Send one and it gets added to the About section.
- Work through the "needs your confirmation" list in the launch plan.

## Updating later
Edit `index.html` and upload it again. The page is plain HTML: each role is one `<li class="stop">` block.
