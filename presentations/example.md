---
marp: true
theme: vt
paginate: true
footer: "Virginia Tech · College of Liberal Arts and Human Sciences"
---

<!-- _class: title -->

# Presentation Title

## Course Name or Event · CLAHS · Virginia Tech

Your Name · Department · Semester Year

---

# Slide with Body Content

This template uses the official Virginia Tech brand palette from [brand.vt.edu](https://brand.vt.edu).

- **Chicago Maroon** `#861F41` — headings, strong text, table headers
- **Burnt Orange** `#E5751F` — accents, list markers, code borders
- **Hokie Stone** `#75787B` — footer, captions, neutral elements

> Blockquotes use Crimson Text — the VT brand serif — for a refined look.

---

# Two-Column Layout

<div style="display:grid; grid-template-columns:1fr 1fr; gap:2.5em; margin-top:0.5em;">
<div>

### Left Column
Use an HTML `<div>` grid for layouts that need side-by-side content.

- Concept A
- Concept B
- Concept C

</div>
<div>

### Right Column
Marp's native `![bg right:40%](image.png)` directive is even easier for image + text layouts.

</div>
</div>

---

# Code Example

Install dependencies and build slides:

```bash
npm install
npm run build        # HTML
npm run build:pdf    # PDF (requires Chrome)
npm run build:pptx   # PowerPoint
```

```python
# Inline code uses maroon-tinted dark background
def greet(name: str) -> str:
    return f"Let's Go, Hokies! Hello, {name}."
```

---

<!-- _class: section -->

# Section Title

Use `<!-- _class: section -->` for a burnt orange section-break slide between major topics.

---

# Background Image Slide

Marp handles image backgrounds natively — no extra CSS needed:

```markdown
![bg right:45%](../assets/your-image.jpg)
```

The VT theme's maroon top-bar is suppressed when using full-bleed backgrounds via `![bg](image.jpg)`.

---

# Tables

| Column A | Column B | Column C |
|----------|----------|----------|
| Row 1    | Data     | Result   |
| Row 2    | Data     | Result   |
| Row 3    | Data     | Result   |

Table headers use Chicago Maroon. Alternating rows use Hokie Stone pale.

---

<!-- _class: stone -->

# Hokie Stone Slide

Use `<!-- _class: stone -->` for a neutral, understated slide — good for supplementary material, acknowledgments, or Q&A prompts.

---

# Speaker Notes

Add notes in HTML comments — they don't appear on the slide:

```markdown
# My Slide

Content visible to the audience.

<!-- Notes only you can see in presenter mode.
     Open presenter view: press P in the browser. -->
```

<!-- 
These are speaker notes for this slide.
Only visible in presenter mode.
-->

---

<!-- _class: title -->

# Thank You

**Questions?**

`your.email@vt.edu` · [your-site.vt.edu](https://vt.edu)

*Ut Prosim — That I May Serve*
