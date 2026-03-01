# Marp Presentation Template

A GitHub template repository for creating beautiful Markdown-based presentations with [Marp](https://marp.app/), pre-configured to run in GitHub Codespaces with the Marp VS Code extension.

---

## ✨ Features

- **Instant Codespace** — open this repo in a browser-based VS Code with Marp already installed
- **Live preview** — see your slides update as you type via the Marp VS Code extension
- **Custom theme** — a ready-to-customize CSS theme in `themes/custom.css`
- **GitHub Actions** — automatically builds HTML, PDF, and PPTX on every push to `main`
- **GitHub Pages** — published slides available as a live website after each push

---

## 🚀 Quick Start

### Option A: GitHub Codespace (recommended)

1. Click **Use this template → Create a new repository**
2. In your new repo, click **Code → Codespaces → Create codespace on main**
3. Wait ~60 seconds for the container to build
4. Open any `.md` file in `presentations/`
5. Click the **preview icon** (top-right) or press `Ctrl+Shift+V` to open the Marp preview pane

### Option B: Local development

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cd YOUR-REPO
npm install
```

Then open in VS Code with the [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode) extension installed.

---

## 📁 Repository Structure

```
.
├── .devcontainer/
│   └── devcontainer.json      # Codespace config (extensions, settings)
├── .github/
│   └── workflows/
│       └── build.yml          # Build + deploy GitHub Action
├── presentations/
│   └── example.md             # Start here — copy to make new decks
├── themes/
│   └── custom.css             # Your custom Marp theme
├── output/                    # Built files (gitignored locally)
├── .marprc.yml                # Marp CLI defaults
└── package.json               # npm scripts
```

---

## 🖊️ Writing Slides

Each `.md` file in `presentations/` is an independent deck. Start every file with:

```markdown
---
marp: true
theme: custom
paginate: true
footer: "Your Name | Title | Date"
---

# First Slide
```

Separate slides with `---`.

### Special slide classes

| Directive | Effect |
|-----------|--------|
| `<!-- _class: title -->` | Dark title slide |
| `<!-- _class: accent -->` | Accent-colored section break |
| `<!-- _backgroundColor: #hex -->` | Per-slide background |
| `<!-- _color: white -->` | Per-slide text color |

### Speaker notes

```markdown
# Slide Title

Slide content here.

<!-- Your speaker notes here. Press P in browser preview for presenter mode. -->
```

---

## 🏗️ Building Slides

| Command | Output |
|---------|--------|
| `npm run build` | HTML files → `output/` |
| `npm run build:pdf` | PDF files → `output/` |
| `npm run build:pptx` | PPTX files → `output/` |
| `npm run build:all` | All three formats |
| `npm run watch` | Rebuild HTML on save |
| `npm run preview` | Open browser preview with hot reload |

---

## 🎨 Customizing the Theme

Edit `themes/custom.css`. The CSS variables at the top control the color palette:

```css
:root {
  --color-primary:   #861F41;  /* Main brand color */
  --color-secondary: #E5751F;  /* Accent color */
}
```

Register your theme in `.marprc.yml` and in the VS Code settings inside `.devcontainer/devcontainer.json` (already done).

---

## 🌐 GitHub Pages

After your first push to `main`, enable GitHub Pages:

1. Go to **Settings → Pages**
2. Set **Source** to **GitHub Actions**

Your presentations will be published at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

---

## 📄 License

MIT — use freely, attribution appreciated.
