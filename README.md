# Programming for Web Development – I Laboratory

> **Course:** Programming for Web Development – I Laboratory  
> **Student:** Nilay Raj  
> **Specialization:** First Year B.Tech Computer Science & Engineering (AIML)  
> **Repository:** [https://github.com/NilayOverp94/Web_Dev_Lab](https://github.com/NilayOverp94/Web_Dev_Lab)

---

## Overview

This repository contains the complete, production-grade solutions for all 13 laboratory practical assignments specified in the **Programming for Web Development – I Laboratory** curriculum. The curriculum spans terminal CLI navigation, Git version control workflows, semantic HTML5 document architecture, CSS custom properties (design tokens), advanced positioning, Flexbox one-dimensional distribution, and CSS Grid two-dimensional layout orchestration.

---

## Laboratory Curriculum & Practicals Index

### Module 1: Terminal & Git Foundations (P1–P4)

| Practical | Title | Focus & Core Mechanics | Folder Link |
|---|---|---|---|
| **P1** | Project Folder and Terminal Navigation | CLI filesystem navigation, directory scaffolding (`mkdir -p`), relative/absolute path traversal, and POSIX file inspection. | [View P1](P1/Readme.md) |
| **P2** | Portfolio Repo with an Initial Commit | Local Git initialization (`git init -b main`), `.gitignore` curation, staging index mechanics, initial release commit, and GitHub remote association. | [View P2](P2/Readme.md) |
| **P3** | Feature-Branch Git Workflow | Isolated branch lifecycle (`feature/*`), atomic commits, branch synchronization, merge integration (`git merge --no-ff`), and branch pruning. | [View P3](P3/Readme.md) |
| **P4** | GitHub README and Version Tags | GFM documentation engineering and Semantic Versioning release management using annotated tags (`git tag -a v1.0.0`). | [View P4](P4/Readme.md) |

---

### Module 2: HTML & CSS Foundations (P5–P9)

| Practical | Title | Focus & Core Mechanics | Folder Link |
|---|---|---|---|
| **P5** | Semantic Bio Page | Accessible document tree utilizing HTML5 semantic tags (`header`, `main`, `section`, `article`, `aside`, `footer`) with clean responsive styling. | [View P5](P5/index.html) |
| **P6** | Full Portfolio Page Structure in Semantic HTML | Comprehensive developer portfolio with multi-tier navigation, hero introduction, about matrix, categorized competencies, project showcase, and contact form. | [View P6](P6/index.html) |
| **P7** | Design Tokens and Typography System in CSS | Centralized CSS custom properties (`:root`) defining modular typography scales (1.25 ratio), semantic color palettes, and 8px baseline spacing scales. | [View P7](P7/index.html) |
| **P8** | Sticky Navbar and Card Overlay using CSS Positioning | Viewport sticky navigation (`position: sticky; top: 0`) and interactive card hover curtains utilizing relative/absolute coordinate contexts. | [View P8](P8/index.html) |
| **P9** | Responsive Navbar and Card Grid using Flexbox | One-dimensional fluid layout implementing responsive navigation, auto-wrapping cards (`flex: 1 1 280px`), and vertical flex card footers (`margin-top: auto`). | [View P9](P9/index.html) |

---

### Module 3: CSS Layout Systems (P10–P13)

| Practical | Title | Focus & Core Mechanics | Folder Link |
|---|---|---|---|
| **P10** | Portfolio Header and Footer with Advanced Flexbox | Multi-level utility and primary navigation header with dynamic `order` restructuring, paired with a complex multi-column responsive footer. | [View P10](P10/index.html) |
| **P11** | Newspaper-Style Three-Column Layout with CSS Grid | Editorial broadsheet architecture utilizing 3-column CSS Grid tracks, multi-column article flows, drop-caps, and editorial typographic hierarchy. | [View P11](P11/index.html) |
| **P12** | Portfolio Projects Grid with Advanced CSS Grid | Asymmetric 12-column Bento project grid utilizing `grid-column: span`, `grid-row: span`, and responsive track adaptations. | [View P12](P12/index.html) |
| **P13** | Choosing Between Flexbox and Grid for a Shared Layout | In-depth architectural evaluation and side-by-side component implementations comparing 1D content-out Flexbox with 2D container-in CSS Grid. | [View P13](P13/index.html) |

---

## Repository Structure

```text
Web_Dev_Lab/
├── P1/                   # Project folder and terminal navigation
│   └── Readme.md
├── P2/                   # Portfolio repo with an initial commit
│   └── Readme.md
├── P3/                   # Feature-branch Git workflow
│   └── Readme.md
├── P4/                   # GitHub README and version tags
│   └── Readme.md
├── P5/                   # Semantic bio page
│   ├── index.html
│   ├── style.css
│   └── P5.png
├── P6/                   # Full portfolio page structure in semantic HTML
│   ├── index.html
│   ├── style.css
│   └── P6.png
├── P7/                   # Design tokens and typography system in CSS
│   ├── index.html
│   ├── style.css
│   └── P7.png
├── P8/                   # Sticky navbar and card overlay using CSS positioning
│   ├── index.html
│   ├── style.css
│   └── P8.png
├── P9/                   # Responsive navbar and card grid using Flexbox
│   ├── index.html
│   ├── style.css
│   └── P9.png
├── P10/                  # Portfolio header and footer with advanced Flexbox
│   ├── index.html
│   ├── style.css
│   └── P10.png
├── P11/                  # Newspaper-style three-column layout with CSS Grid
│   ├── index.html
│   ├── style.css
│   └── P11.png
├── P12/                  # Portfolio projects grid with advanced CSS Grid
│   ├── index.html
│   ├── style.css
│   └── P12.png
├── P13/                  # Choosing between Flexbox and Grid for a shared layout
│   ├── index.html
│   ├── style.css
│   └── P13.png
└── README.md             # Root course documentation & index
```

---

## Technologies & Methodologies

- **Markup:** HTML5 (Living Standard, W3C Semantic Validation)
- **Styling:** CSS3, CSS Custom Properties (`:root`), Flexbox, CSS Grid
- **Version Control:** Git CLI, GitHub, Semantic Versioning (SemVer)
- **Development Tools:** Visual Studio Code, Unix / Zsh Terminal, Chrome DevTools

---

## Verification & Local Preview

To inspect and test any of the web practicals locally:
1. Clone this repository:
   ```bash
   git clone https://github.com/NilayOverp94/Web_Dev_Lab.git
   cd Web_Dev_Lab
   ```
2. Open any practical in your browser:
   ```bash
   # Example: Open Practical 11 (Newspaper Layout)
   open P11/index.html
   ```

---

## Author

**Nilay Raj**  
First Year B.Tech Computer Science & Engineering (AIML)  
GitHub: [@NilayOverp94](https://github.com/NilayOverp94) &middot; Email: [nilayraj713@gmail.com](mailto:nilayraj713@gmail.com)
