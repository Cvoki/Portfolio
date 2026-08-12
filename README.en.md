<div align="right">

[Srpski](README.md) · **English**

</div>

# Luka Cvoro — Portfolio

Personal site and CV. Oracle APEX & PL/SQL developer based in Belgrade.

**Live:** [lukacvoro.netlify.app](https://portfoliolukacvoro.netlify.app/) · **LinkedIn:** [luka-cvoro](https://www.linkedin.com/in/luka-cvoro-3b2194197/) · **Email:** [lukac95@gmail.com](mailto:lukac95@gmail.com)

---

## What this is

A single-page portfolio with no framework at all — plain HTML, CSS and JavaScript in one file. No build step, no `node_modules`, no dependencies. Open `index.html` and it runs.

The idea was for the site to not just *describe* what I do, but to **show** it: since I work with databases, filtering the tech stack prints a real SQL query, and submitting a form shows the `INSERT` that would store it.

## What it does

| | |
|---|---|
| **Bilingual** | The whole site in Serbian and English — one click, no page reload. Text, dates, code samples and error messages all switch. |
| **Live SQL console** | The filters above the tech list print an actual `SELECT ... WHERE ... ORDER BY` with a row count that updates as you choose. |
| **GitHub projects** | Repositories are pulled live from the GitHub API. A new project shows up on its own — no code change, no redeploy. |
| **Timeline** | Experience and education with bullet points per role, active positions marked. |
| **Forms** | Contact and quote request, with per-field validation and submission through Netlify Forms — no backend. |
| **Date picker** | A custom one, because the native `input[type=date]` ignores the site's language. Formats as `dd.mm.yyyy.` or `dd/mm/yyyy`. |

## Built with

`HTML5` · `CSS3` (Grid, Flexbox, custom properties) · `JavaScript` (ES6+, no libraries) · `GitHub REST API` · `Netlify Forms`

No jQuery, no React, no Tailwind. Deliberately — for a site this size they would be more weight than help.

## Structure

```
.
├── index.html      # the whole site: markup, styles, logic, translations
├── luka.jpg        # photo (400×400)
├── og.png          # link preview image (1200×630)
├── README.md       # Serbian version
└── README.en.md    # this file
```

## Running it

```bash
git clone https://github.com/Cvoki/portfolio.git
cd portfolio
```

Open `index.html` in a browser — that's it.

For a local server (needed if you want to test form submission):

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

> **Note:** form submission only works on the deployed site, since it relies on Netlify Forms.

## Deployment

The site runs on Netlify, connected to this repository — every `push` to `main` triggers a new deploy.

For forms, enable **Forms → Enable form detection** once in the Netlify dashboard, then redeploy. Notifications are configured under *Notifications → Form submission notifications*.

## Editing content

Everything editable lives in the `<script>` block at the bottom of `index.html`, in a handful of arrays:

| What you change | Where |
|---|---|
| All text translations | `const T = { sr: {...}, en: {...} }` |
| Work experience | `const XP = [...]` |
| Education | `const EDU = [...]` |
| Languages | `const JEZICI = [...]` |
| Tech stack and levels | `const TEH = [...]` |
| Code samples | `const PRIMERI = {...}` |

Every text field takes the shape `{sr: "...", en: "..."}` — add both and the translation works by itself.

## License

The code is free to use and learn from. The content (biography, photo, copy) is not — that part is mine.

---

<sub>If you'd like to work together or have a question — <a href="mailto:lukac95@gmail.com">get in touch</a>.</sub>
