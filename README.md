# Personal academic website

Plain static HTML/CSS/JS — no build step, no framework. Pages:

- `index.html` — home / about
- `research.html` — research overview + project cards
- `projects/co-cu100-field-effects.html` — first case study (CO/Cu(100) field effects)
- `publications.html`
- `cv.html`
- `contact.html`

Everything in `[Your Name]` / `[square brackets]` is a placeholder — fill
those in across all pages before publishing (name, university, bio text,
publications, CV entries, contact links). The CV page links to
`assets/cv.pdf`, which doesn't exist yet — drop your CV PDF there, or
remove the "Download PDF" button in `cv.html`.

## Preview locally

```
cd personal-website
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new **public** repo on GitHub, e.g. `aritriroyiitb.github.io`
   (that exact name gives you a site at `https://aritriroyiitb.github.io/`;
   any other repo name serves at `https://aritriroyiitb.github.io/reponame/`,
   in which case every internal link above still works since they're all
   relative paths).
2. From this directory:
   ```
   git remote add origin git@github.com:aritriroyiitb/aritriroyiitb.github.io.git
   git branch -M main
   git push -u origin main
   ```
3. In the repo's Settings &rarr; Pages, set Source = "Deploy from a
   branch", Branch = `main`, folder = `/ (root)`. GitHub Pages will build
   and give you the live URL within a minute or two.
4. Optional custom domain: Settings &rarr; Pages &rarr; Custom domain, plus
   a `CNAME` DNS record at your domain registrar pointing to
   `aritriroyiitb.github.io`.

## Adding a new project later

1. Add a new `<div class="card">...</div>` block to `research.html`.
2. Copy `projects/co-cu100-field-effects.html` as a starting template for
   the new project's page.
3. Drop any GIFs/PNGs into `assets/img/` or `assets/figures/`.
