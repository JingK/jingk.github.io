# Personal website

A simple one-page personal site in plain HTML and CSS. There's no build step and nothing to install, so GitHub Pages can serve the files as they are.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The page itself: intro, About, Projects, Contact |
| `styles.css` | All styling. Colors are set at the top of the file |
| `favicon.svg` | The small icon in the browser tab |
| `404.html` | Shown when someone visits a page that doesn't exist |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is |

## Make it yours

1. In `index.html`, replace every `Your Name`, `you@example.com`, and `your-username`, then rewrite the placeholder text.
2. In `favicon.svg`, change `YN` to your initials. Do the same for the `YN` link at the top of `index.html`.
3. To change colors, edit the variables at the top of `styles.css`. The second block is for dark mode.

## Preview on your computer

From this folder, run:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.

## Publish with GitHub Pages

This repository is named `jingk.github.io`, which is what puts the site at `https://jingk.github.io/`. It has to stay **public** for Pages to work on a free GitHub plan.

1. In the repository, go to **Settings → Pages**.
2. Under **Build and deployment**, check that **Source** is **Deploy from a branch** with `main` and `/ (root)`. If not, set it and click **Save**.
3. After a minute or two the site is live at `https://jingk.github.io/`.

Every push to `main` updates the site automatically.

## Use your own domain (optional)

1. Buy a domain from a registrar such as Cloudflare, Porkbun, or Namecheap.
2. In **Settings → Pages → Custom domain**, enter your domain (for example `yourname.com`) and click **Save**. GitHub adds a `CNAME` file to the repository for you. This is a new commit on `main`, so run `git pull` before you next push from your computer, and don't delete the `CNAME` file.
3. At your registrar, add these DNS records:
   - For `yourname.com`, four `A` records pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`.
   - For `www.yourname.com`, a `CNAME` record pointing to `jingk.github.io`.
4. DNS can take up to a day to update. When **Settings → Pages** shows "DNS check successful", tick **Enforce HTTPS**. If the box is greyed out, GitHub is still setting up the certificate, which can take up to 24 hours.

All links in the site are relative, so nothing in the code needs to change when you switch to your own domain.
