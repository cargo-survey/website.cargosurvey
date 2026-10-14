# website.cargosurvey

The public website at https://cargosurvey.co.za: a one-page introduction to CargoSurvey and its privacy policy. Plain static HTML and CSS with no build step, hosted on GitHub Pages.

## Files

- `index.html`: home page
- `privacy.html`: privacy policy (POPIA). Meta asks for a privacy policy URL for the WhatsApp app.
- `styles.css`: shared styles, with light and dark mode
- `CNAME`: the custom domain GitHub Pages serves
- `.nojekyll`: serve the files as they are

## Editing

Open `index.html` in a browser to preview it. Commit to `main` and GitHub Pages republishes within a minute or two.

The company details (registration number, address, contact email and phone) appear in both pages. Keep them identical to the CIPC registration, because Meta's business verification compares them.

## Hosting setup (once)

1. In the repo: **Settings → Pages → Build and deployment**: Source **Deploy from a branch**, branch `main`, folder `/ (root)`. Custom domain: `cargosurvey.co.za`.
2. At the domain registrar, add DNS records:
   - `A` records for `cargosurvey.co.za` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `cargo-survey.github.io`
3. Once the DNS check passes in Settings → Pages, tick **Enforce HTTPS**.

## Meta domain verification

If Meta asks to verify the domain with a meta tag, paste the tag it gives you where `index.html` says `META_DOMAIN_VERIFICATION`, then commit.
