# Publishing the Fall 2026 textbook refresh (from this VS Code clone)

The revised textbook source has been synced into this folder (July 2026).
To publish, open the terminal in VS Code and run:

    git checkout main
    git pull                                  # make sure you're current
    git rm _config.yml _toc.yml               # legacy Jupyter Book v1 files, replaced by myst.yml
    git rm module-01-intro/index.md module-02-infrastructure/index.md \
           module-03-design/index.md module-04-databases/index.md \
           module-05-accessibility/index.md module-06-analytics/index.md \
           module-07-visualization/index.md module-08-search/index.md \
           module-09-security/index.md module-10-copyright/index.md \
           module-11-autonomous/index.md module-12-ai/index.md
           # ^ old chapter filenames, replaced by meaningful names (e.g. search-and-retrieval.md)
    git add -A
    git commit -m "Fall 2026 refresh: currency corrections, AI thread, Module 13, meaningful URLs, working notebook"
    git push

GitHub Actions will rebuild and deploy the site automatically (~3-5 minutes).
Check progress under the repo's "Actions" tab.

Notes:
- If you skip the two `git rm` steps, nothing breaks (myst.yml explicitly
  excludes all the old files), but the repo stays tidier if you remove them.
- Heads-up: page URLs changed (that was the point: Module 1 was unreachable
  and chapters lived at /index-1 ... /index-11). Update any Canvas deep links
  after publishing.
- Delete this file whenever you like; it's just instructions.
