# UK VAT Guide (backlink content page)

A single static page (`index.html`) with a clean, modern design and one dofollow
link to **freevatcalculator.co.uk** using the anchor text **VAT Calculator**.

## Files
- `index.html` — the whole page. Self contained, no build step, no dependencies.

## Deploy with GitHub + Vercel

1. On GitHub, create a new repository (for example `vat-guide`). Leave "Add a README" unticked.
2. Add `index.html` to the repo. Easiest way: on the repo page click **Add file > Upload files**, drop in `index.html`, then **Commit changes**.

   Or from a terminal:
   ```
   git init
   git add index.html
   git commit -m "Add VAT guide page"
   git branch -M main
   git remote add origin https://github.com/AbdulHadi013/vat-guide.git
   git push -u origin main
   ```
3. Go to vercel.com, sign in with GitHub, click **Add New > Project**, import the repo, and click **Deploy**. No settings are needed for a plain `index.html`.
4. Within a few seconds you get a live address like `https://vat-guide.vercel.app`.

## Do this right after the first deploy

- Open `index.html`, find `REPLACE-WITH-YOUR-VERCEL-URL`, and swap in your real Vercel
  address, then push again. This sets the page's own canonical address so Google
  indexes the Vercel page itself and not your money site.
- The link to freevatcalculator.co.uk is a normal dofollow link, so it passes link
  value. If you want it to open in a new tab, add `target="_blank" rel="noopener"` to
  that one link.

## Good to know

- The page is static free content, so Vercel's free Hobby plan is fine for hosting it.
- Every future `git push` to `main` redeploys the site automatically.
- To get it indexed faster, submit the Vercel URL in Google Search Console once it is live.
