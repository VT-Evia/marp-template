# Marp Presentation Template

This repository lets you create **professional slide presentations by writing plain text**. Instead of clicking around in PowerPoint or Google Slides, you write your content in a simple format called Markdown, and the system turns it into a polished slide deck automatically.

This might sound unusual at first, but it has real advantages for communicators:

- Your content and your design are completely separate — change the look of every slide at once by editing one file
- Your presentations live in the same place as your other course files and are version-controlled (you can always go back to an earlier draft)
- Output is generated automatically — push your changes to GitHub and the presentation is built and published for you

---

## What Is Marp?

**Marp** is a free, open-source tool that converts Markdown files into slide presentations. Markdown is the same plain-text formatting used in course management systems, GitHub, and many content platforms — if you've ever used `**bold**` or `# Heading` in a text editor, you already know the basics.

A Marp slide file looks like this:

```
---
marp: true
---

# My First Slide

This is the content of slide one.

---

# My Second Slide

- Bullet point one
- Bullet point two
```

Each `---` on its own line creates a new slide. That's really all there is to it.

---

## Getting Started (No Installation Required)

The easiest way to use this template is through **GitHub Codespaces** — a full coding environment that runs in your browser. You don't need to install anything on your computer.

### Step 1 — Copy this template

1. Click the green **Use this template** button at the top of this page
2. Select **Create a new repository**
3. Give your repository a name (e.g., `comm-4564-presentation`)
4. Leave it set to **Public** and click **Create repository**

### Step 2 — Open your Codespace

1. In your new repository, click the green **Code** button
2. Click the **Codespaces** tab
3. Click **Create codespace on main**
4. Wait about 60 seconds while the environment loads in your browser

You'll see a VS Code editor open in your browser. This is where you'll write your slides.

### Step 3 — Open the example presentation

In the left sidebar, expand the `presentations/` folder and click **example.md** to open it.

### Step 4 — Preview your slides

Click **Terminal → New Terminal** in the menu bar and run:

```bash
npm run preview
```

This builds your slides and opens them in a browser tab that updates automatically as you save changes.

---

## Writing Your Presentation

### Starting a new deck

1. In the `presentations/` folder, right-click and choose **New File**
2. Name it something like `my-presentation.md`
3. Copy the front matter block from `example.md` at the top:

```
---
marp: true
theme: vt
paginate: true
footer: "Your Name · Virginia Tech · Date"
---
```

Everything after this block is your slide content.

### Slide structure

| What you type | What it does |
|---------------|--------------|
| `---` on its own line | Starts a new slide |
| `# Heading` | Large slide title |
| `## Subheading` | Smaller heading |
| `- Item` | Bullet point |
| `**bold text**` | Bold |
| `*italic text*` | Italic |

### Special slide types

Add a comment directly above a slide's content to change its style:

```
<!-- _class: title -->
# Cover Slide Title
## Subtitle
```

```
<!-- _class: section -->
# Section Break
```

### Speaker notes

Anything inside `<!-- -->` comment tags won't appear on the slide but will be visible to you in presenter mode:

```
# My Slide

Content the audience sees.

<!-- Notes only I can see during the presentation. -->
```

### Using Images

#### Where to store your image files

Put images in the `assets/` folder at the root of your repository. From any file inside `presentations/`, reference them with a relative path starting with `../assets/`:

```
marp-template/
├── assets/
│   ├── sample.png       ← drop your images here
│   └── my-photo.jpg
└── presentations/
    └── example.md       ← reference as ../assets/my-photo.jpg
```

#### Inline image (inside slide content)

Standard Markdown image syntax places the image within the slide's text area:

```
![A descriptive alt text](../assets/my-photo.jpg)
```

You can control the size with HTML attributes:

```
<img src="../assets/my-photo.jpg" alt="Description" width="400">
```

#### Full-bleed background image

Place an image behind the entire slide by adding `bg` to the alt text:

```
![bg](../assets/my-photo.jpg)
```

Marp automatically scales and crops the image to fill the slide. The VT theme hides the maroon top-bar when a full background is used.

#### Split background — image beside text

Use `bg right` or `bg left` to fill half the slide with an image while keeping text on the other half. An optional percentage controls the split:

```
![bg right:45%](../assets/my-photo.jpg)

# Slide Title

Your text content goes here on the left side.
```

```
![bg left:40%](../assets/my-photo.jpg)

# Slide Title

Your text content goes here on the right side.
```

---

## Sharing Your Presentation Online

Every time you save changes and **commit** them to GitHub, the presentation is automatically built and published to a public web address. This means you can share a link to your slides without anyone needing to download a file.

Your presentation will be available at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

To enable this the first time:
1. Go to your repository on GitHub
2. Click **Settings → Pages**
3. Under **Source**, select **GitHub Actions**
4. Click Save, then push any change to trigger the first build

---

## Files in This Repository

```
marp-template/
├── presentations/         ← Put your .md slide files here
│   └── example.md         ← Start here
├── assets/                ← Put your images here
│   └── sample.png         ← Example image included with the template
├── themes/
│   └── vt.css             ← Virginia Tech color theme (don't edit unless you want to customize)
├── .marprc.yml            ← Tells Marp which theme to use by default
├── package.json           ← Lists the software this project needs
└── README.md              ← This file
```

You'll spend almost all of your time inside the `presentations/` folder.

---

## Getting Help

- **Marp documentation:** [marp.app](https://marp.app)
- **Markdown reference:** [markdownguide.org/basic-syntax](https://www.markdownguide.org/basic-syntax/)
- **GitHub Codespaces guide:** [docs.github.com/codespaces](https://docs.github.com/en/codespaces)

If something isn't working, check that:
1. Your file is saved (look for a dot next to the filename in the tab)
2. The front matter block at the top includes `marp: true`
3. Each slide is separated by `---` on its own line with a blank line before and after it
