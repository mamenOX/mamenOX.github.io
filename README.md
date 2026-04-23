# Matthew Amengual — Personal Academic Website

## Overview

This is a static HTML website hosted on GitHub Pages. There are no build tools, frameworks, or dependencies — just plain HTML and CSS.

- **Live site:** https://mattamengual.net/ (also accessible at https://mamenox.github.io/)
- **GitHub repo:** https://github.com/mamenOX/mamenOX.github.io

---

## File Structure

```
website/
├── index.html      # The entire website (single page)
├── style.css       # All styles
├── book1.jpg       # Cover: Politicized Enforcement in Argentina (Cambridge UP, 2016)
├── book2.jpg       # Cover: Communities, Mines, and Distributive Politics (OUP, 2024)
└── README.md       # This file
```

---

## How to Make Changes

Edit `index.html` and/or `style.css` directly — there is no build step.

### Pushing changes to GitHub (which updates the live site)

Open Terminal, navigate to this folder, then run:

```bash
cd "/Users/mamengual/Desktop/AI Folders/website"
git add index.html style.css
git commit -m "Describe your changes here"
git pull --rebase origin main   # fetch any remote changes first
git push origin main
```

> **Note:** Always run `git pull --rebase origin main` before `git push` to avoid rejection errors. GitHub Pages automatically redeploys after every push — allow 1–5 minutes for the live site to update. If it looks unchanged, try a hard refresh (Cmd+Shift+R).

If you add new image files, include them in the `git add` command:

```bash
git add index.html style.css newimage.jpg
```

---

## Google Analytics

The site uses GA4. The tracking ID is **G-EJEKPDSZEV**. The snippet is in the `<head>` of `index.html`.

---

## Key Sections in index.html

| Section ID        | Content |
|-------------------|---------|
| `#bio`            | Short biography paragraph |
| `#books`          | Book covers and citations |
| `#working-papers` | Completed working papers |
| `#articles`       | Peer-reviewed journal articles |
| `#other`          | Book chapters and other publications |

---

## Notes for Future Edits

- **New publication:** Add a `<li>` entry in the appropriate section. Follow the existing format: linked title, co-authors with links, journal name in `<span class="pub-venue">`, volume(issue), year.
- **"Forthcoming" articles:** Once published, replace `forthcoming` with `volume(issue), year` and verify the DOI link is correct.
- **Co-author links:** Check periodically — academics move institutions. Update the `href` on their name.
- **Book images:** Sized at 120px wide via `.book-item img` in `style.css`. Adjust the `width` value there to resize.
- **Email address:** Appears in the `<p class="contact">` block near the top of `index.html`.
