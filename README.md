# INF 110: Foundations of Informatics — Interactive Textbook

The online textbook for **INF 110 Foundations of Informatics** at Dominican University (Dr. Timothy D. Bowman), built with [Jupyter Book / MyST](https://mystmd.org/) and published via GitHub Pages.

**Live site:** https://tdbowman.github.io/110informatics.github.io/

## Structure

- `myst.yml` — the single source of configuration **and the table of contents**. Add/remove/reorder chapters here.
- `intro.md` — the landing page.
- `module-NN-topic/` — one folder per module; the chapter file inside carries a meaningful name (e.g., `module-08-search/search-and-retrieval.md`) so page URLs are readable and stable.
- `module-07-visualization/hands-on-charts.ipynb` — the interactive notebook. Its outputs are committed, so charts render on the static site; students can also open it in Colab.
- `data/` — datasets used by notebooks (vendored so the book has no third-party data dependencies).
- `glossary.md`, `references.md`, `course-wrapup.md` — back matter.
- `.github/workflows/deploy.yml` — builds and deploys the site on every push to `main` (uses the npm `jupyter-book` CLI, i.e., the MyST engine).

## Editing workflow

1. Edit or add markdown/notebook files.
2. If you added or renamed a file, update `toc:` in `myst.yml`.
3. Preview locally (optional): `npm install -g jupyter-book`, then `jupyter-book start`.
4. Commit and push to `main` — GitHub Actions rebuilds and deploys automatically (takes a few minutes).

### Re-running the notebook

If you edit `hands-on-charts.ipynb` code, re-execute it before committing so the site shows fresh outputs:

```bash
pip install jupyter pandas matplotlib
jupyter nbconvert --to notebook --execute --inplace module-07-visualization/hands-on-charts.ipynb
```

## Annual refresh checklist (start of each offering)

- [ ] Anything marked **"as of"** in the text — legal statuses, AI landscape tables, deployment snapshots
- [ ] The 📌 case study boxes (designed to be swapped without touching surrounding prose)
- [ ] Social-media user numbers in the notebook
- [ ] Run a link check (consider a `lychee` GitHub Action)
- [ ] The revision date in `intro.md` and `about-this-book.md`

## Requirements

`requirements.txt` covers the Python packages needed to run the notebooks locally. The site build itself needs only Node (the deploy workflow handles it).

---

*Last major revision: Summer 2026 (for the Winter 2027 offering) — full audit, currency corrections, AI-thread integration, Modules 1 slug fix and 13 added.*
