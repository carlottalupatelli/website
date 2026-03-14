# Carlotta A. Lupatelli, PhD — Personal Website

**Live:** https://carlottalupatelli.github.io/carlotta-website/

Personal academic and professional website for Carlotta A. Lupatelli, PhD — plant pathologist, proteomics researcher, and science communicator based in Barcelona, Spain.

---

## Tech stack

Pure HTML, CSS, and JavaScript — no build tools, no frameworks, no package manager. Open any `.html` file directly in a browser to preview locally, or use a simple server:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

Deployment is automatic: pushing to `main` triggers GitHub Actions (`.github/workflows/deploy.yml`), which deploys to GitHub Pages.

---

## Project structure

```
carlotta-website/
├── .github/workflows/deploy.yml   # GitHub Actions → GitHub Pages
├── assets/                        # Images, PDFs, and downloadable files
├── css/style.css                  # Single shared stylesheet
├── js/main.js                     # Scroll reveal and nav behaviour
├── teaching/                      # Course detail pages
│   ├── image-analysis.html
│   ├── critical-thinking.html
│   ├── master-supervision.html
│   └── welcome-day.html
├── index.html                     # Home / About
├── publications.html              # Research publications
├── projects.html                  # R&D projects
├── teaching.html                  # Teaching overview
├── cv.html                        # Curriculum Vitae
├── blog.html                      # Blog
├── contact.html                   # Contact
└── favicon.svg
```

---

## Pages

**Home** (`index.html`) — Hero section, professional summary, and navigation cards.

**Publications** (`publications.html`) — Peer-reviewed papers and other research outputs, including work in *Scientific Reports* (2025) and *Computational and Structural Biotechnology Journal* (2023).

**Projects** (`projects.html`) — Research and industry projects spanning ML image analysis, membrane proteomics, biocontrol product development, and regulatory affairs.

**Teaching** (`teaching.html`) — Overview of teaching activities, each linking to a dedicated detail page:
- *Image analysis for biology* — 12-hour MSc course on biological imaging pipelines
- *Critical thinking and interactive learning* — 4-hour figure analysis session for MScBOOST students
- *Master's thesis supervision* — 6-month proteomics project supervision
- *Interactive learning and student integration* — Welcome Day Treasure Hunt co-designed for incoming MSc students

**CV** (`cv.html`) — Work experience, education, and skills. Print-friendly.

**Blog** (`blog.html`) — Science communication and writing.

**Contact** (`contact.html`) — Email, LinkedIn, and contact form.

---

## Design system

All pages share `css/style.css`. CSS custom properties in `:root` control the entire colour palette — always use variables, never hardcoded hex values.

| Token | Value | Use |
|---|---|---|
| `--primary` | `#00796b` | Teal 700 — main brand colour |
| `--accent` | `#4caf50` | Green 500 — highlights and links |
| `--surface` | `#ffffff` | Card backgrounds |
| `--background` | `#f5f5f5` | Page background |
| `--text` | `#212121` | Body text |
| `--text-secondary` | `#757575` | Subtitles, metadata |

**Fonts:** Archivo (headings) + Space Grotesk (body) — loaded via Google Fonts CDN.

**Layout:** sticky nav → hero/header → content cards (`.publication`) → footer. When adding a new page, copy the nav and footer from any existing page.

---

## Notes on large assets

Files over 100 MB cannot be hosted on GitHub. Large PowerPoint files should be converted to PDF before committing:

```bash
/Applications/LibreOffice.app/Contents/MacOS/soffice \
  --headless --convert-to pdf "assets/file.pptx" --outdir assets/
```

`*.pptx` is listed in `.gitignore`.

---

## Contact

- **Email:** carlotta.aurora.lupatelli@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/carlotta-aurora-lupatelli
- **Google Scholar:** https://scholar.google.com/citations?user=jyS56jgAAAAJ

---

All content © 2025 Carlotta A. Lupatelli.
