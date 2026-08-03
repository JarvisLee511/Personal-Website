# Personal website — Che-Wei Lee

Single-page portfolio site. Dark/light, scroll-driven, Traditional Chinese copy.

**🌐 <https://jarvislee511.github.io/Personal-Website/>**

---

## What is here

One `index.html` with the whole site in it — hero, about, experience, skills,
projects, extracurriculars, contact — plus a lightbox for the project imagery.
No build step, no framework, no bundler.

```
index.html                  the entire site: markup, styles, behaviour
js/gsap.min.js              animation
js/ScrollTrigger.min.js     scroll-linked reveals
js/ScrollSmoother.min.js    smooth scrolling
js/lucide.min.js            icons
*.png / *.jpg / *.jpeg      project screenshots and backgrounds
```

Vendored libraries rather than CDN links, so the site keeps working if a CDN
changes or goes down.

## Notes

- **Theme** — dark by default with a light mode; hero contrast is handled
  separately per theme rather than inherited, because the light hero sits over a
  photographic background.
- **No gradient text.** An earlier pass used a gradient headline; it was removed
  in favour of solid type that stays legible in both themes.
- **Analytics** — Google Analytics 4 is wired in, so section views and résumé
  clicks are measurable rather than guessed at.
- **Copy is Traditional Chinese (Taiwan)** and terminology is kept consistent
  across sections (運動分析 / 公有雲 / 市佔 / 資料管線).

## Running it

It is a static file. Open `index.html`, or serve the folder if you want the
scroll behaviour to match production exactly:

```bash
python -m http.server 8000
```

## Deployment

GitHub Pages from the default branch, root path. Pushing to `main` publishes.
