# INF 110: Foundations of Informatics - Interactive Textbook

An interactive online textbook built with [Jupyter Book](https://jupyterbook.org/) for INF 110 at Dominican University.

## 🚀 Quick Start

### Prerequisites

- Python 3.9 or higher
- Git

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/inf110-textbook.git
   cd inf110-textbook
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Build the book**
   ```bash
   jupyter-book build .
   ```

5. **View locally**
   Open `_build/html/index.html` in your browser

---

## 📦 Deploying to GitHub Pages

### Option 1: Manual Deployment

1. Build the book locally:
   ```bash
   jupyter-book build .
   ```

2. Use `ghp-import` to publish:
   ```bash
   pip install ghp-import
   ghp-import -n -p -f _build/html
   ```

### Option 2: Automatic Deployment with GitHub Actions (Recommended)

Create `.github/workflows/deploy.yml`:

```yaml
name: deploy-book

on:
  push:
    branches:
      - main

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      
      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: '3.11'
      
      - name: Install dependencies
        run: |
          pip install -r requirements.txt
      
      - name: Build the book
        run: |
          jupyter-book build .
      
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: '_build/html'

  deploy:
    needs: build
    runs-on: ubuntu-latest
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

Then in your repository settings:
1. Go to **Settings → Pages**
2. Under "Build and deployment", select **GitHub Actions**

---

## 📁 Project Structure

```
inf110-textbook/
├── _config.yml              # Jupyter Book configuration
├── _toc.yml                 # Table of contents
├── intro.md                 # Landing page
├── about-this-book.md       # About page
├── how-to-use.md            # User guide
├── requirements.txt         # Python dependencies
├── references.bib           # Bibliography (create as needed)
├── glossary.md              # Glossary (create as needed)
├── _static/
│   └── custom.css           # Custom styling
├── images/                  # Shared images
│   ├── logo.png
│   └── informatics-venn.png
└── module-XX-name/          # Each module folder
    ├── index.md             # Module introduction
    ├── topic-1.md           # Content pages
    ├── topic-2.md
    └── hands-on.ipynb       # Interactive notebooks
```

---

## ✏️ Adding Content

### Adding a New Module

1. Create a new folder: `module-XX-name/`
2. Add an `index.md` for the module introduction
3. Add content pages (`.md`) and notebooks (`.ipynb`)
4. Update `_toc.yml` to include the new module

### MyST Markdown Tips

**Admonitions (callout boxes):**
```markdown
```{admonition} Title Here
:class: tip  # or note, warning, seealso
Content goes here.
```
```

**Grid layouts:**
```markdown
::::{grid} 1 1 2 2
:gutter: 3

:::{grid-item-card} Card Title
Card content
:::

::::
```

**Images:**
```markdown
```{image} ../images/filename.png
:alt: Description for accessibility
:width: 400px
:align: center
```
```

---

## 🔧 Configuration

### Key settings in `_config.yml`:

| Setting | Description |
|---------|-------------|
| `title` | Book title (appears in header) |
| `author` | Your name |
| `repository.url` | Your GitHub repo URL |
| `html.baseurl` | Your GitHub Pages URL |
| `launch_buttons.binderhub_url` | URL for Binder launches |
| `execute.execute_notebooks` | `auto`, `force`, `off`, or `cache` |

### Enabling Binder

1. Ensure `requirements.txt` includes all dependencies
2. Set `launch_buttons.binderhub_url` in `_config.yml`
3. Users can click the Binder button to launch notebooks in the cloud

---

## 📝 For Canvas Integration

### Embedding in Canvas Pages

You can link to specific pages or embed them:

**Direct link:**
```
https://yourusername.github.io/inf110-textbook/module-07-visualization/index.html
```

**Embed in Canvas (iframe):**
```html
<iframe src="https://yourusername.github.io/inf110-textbook/module-07-visualization/hands-on-charts.html" 
        width="100%" 
        height="800px" 
        frameborder="0">
</iframe>
```

### Module Introduction Template for Canvas

You can keep module introductions in both places:
- **Canvas**: For assignment links, due dates, discussion forums
- **Jupyter Book**: For content, readings, and interactive elements

Or use the Jupyter Book as the canonical source and link to it from Canvas.

---

## 🤝 Contributing

Suggestions and corrections are welcome! Please open an issue or submit a pull request.

---

## 📄 License

[Add your preferred license here]

---

## 🙏 Acknowledgments

- Built with [Jupyter Book](https://jupyterbook.org/)
- Styled with [Sphinx Book Theme](https://sphinx-book-theme.readthedocs.io/)
- Interactive notebooks powered by [Binder](https://mybinder.org/)
