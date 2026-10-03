# Sanjib Samadder — Portfolio

[![Live site](https://img.shields.io/badge/live-sanjibsamadder.github.io-1D5FD6?style=flat-square)](https://sanjibsamadder.github.io)
[![Hosted on GitHub Pages](https://img.shields.io/badge/hosted%20on-GitHub%20Pages-111418?style=flat-square&logo=github)](https://pages.github.com/)
![Stack](https://img.shields.io/badge/stack-HTML%20%7C%20CSS%20%7C%20JS-B5690A?style=flat-square)

> A single-page portfolio with a terminal / IDE aesthetic, showcasing my work in data science, data analysis and data visualisation.

**Live site:** [sanjibsamadder.github.io](https://sanjibsamadder.github.io)

---

## About

I'm a data analyst and data scientist with around nine years of experience across finance, manufacturing and research consultancy, and a freelancer on Upwork. This site brings together selected projects, my technical stack and contact details in one place.

Each section is styled as a file in a code editor (`hero.py`, `skills.py`, `projects.py`, `contact.py`), and each project card looks like a notebook or script window.

## Features

- **IDE-style layout**: sticky tab bar, window-chrome section headers and monospaced typography.
- **Animated hero**: a `<canvas>` scatter plot with a regression line that draws itself on load.
- **Filterable project gallery**: switch between *Data Science*, *Data Analysis* and *Data Visualization* without a page reload.
- **Scroll-aware navigation**: the active tab updates as you scroll (via `IntersectionObserver`).
- **Responsive**: works from large desktop screens down to phones.
- **Accessible**: visible focus states, ARIA roles on the filter tabs and `prefers-reduced-motion` support.
- **Zero dependencies**: no framework, no build step and no package manager. Only Google Fonts are loaded externally.

## Tech stack

| Layer | Details |
| --- | --- |
| Markup | Semantic HTML5 |
| Styling | Vanilla CSS with custom properties (design tokens) |
| Behaviour | Vanilla JavaScript (filtering, `IntersectionObserver`, Canvas API) |
| Fonts | [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk), [Inter](https://fonts.google.com/specimen/Inter), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) |
| Hosting | GitHub Pages |

## Project structure

```
.
├── index.html      # The entire site: markup, styles and scripts
└── README.md
```

Any additional assets (profile picture, dashboard screenshots and so on) live alongside `index.html`. Note that GitHub Pages is case-sensitive, so the entry file must be named `index.html` in lowercase.

## Run locally

No installation is required.

```bash
# Clone the repository
git clone https://github.com/sanjibSamadder/sanjibSamadder.github.io.git
cd sanjibSamadder.github.io

# Option 1: open the file directly
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Option 2: serve it locally
python -m http.server 8000
# then visit http://localhost:8000
```

## Customising

**Theme colours** are defined as CSS variables at the top of the `<style>` block:

```css
:root {
  --accent-blue:  #1D5FD6;
  --accent-amber: #B5690A;
  --surface:      #F5F7FA;
  --text:         #111418;
}
```

**Adding a project:** copy an existing `<article class="project-card">` block inside the project grid and update:

1. `data-category`: one of `data-science`, `data-analysis` or `data-visualization`
2. The filename and category badge in `.project-card-head`
3. The title, description, tags and links

The filter buttons pick up the new card automatically.

## Deployment

The site is deployed with **GitHub Pages**. Every push to the default branch triggers a rebuild, and changes are usually live within a minute or two.

1. Go to **Settings → Pages**.
2. Under **Source**, select **Deploy from a branch**.
3. Choose the default branch and the `/ (root)` folder.

If a deployment fails with an infrastructure or runner error rather than a problem with the code, pushing a trivial commit normally triggers a clean re-run.

## Selected projects

| Project | Category | Tools |
| --- | --- | --- |
| [Customer Segmentation: K-Means vs. DBSCAN vs. GMM](https://github.com/sanjibSamadder/customer-segmentation-kmeans-dbscan-gmm) | Data Science | scikit-learn, PCA |
| [Lead & Income Predictor](https://github.com/sanjibSamadder/ml-lead-income-cost-prediction) | Data Science | Python, gradient boosting, Streamlit |
| [COVID-19 Chest X-Ray Classification](https://github.com/sanjibSamadder/COVID-19-Chest-X-Ray-Classification-Dese-CNN-Deep-CNN-RNN) | Data Science | Keras, neural networks |
| [Retail Sales & Basket Analysis](https://github.com/sanjibSamadder/sql-retail-basket-analysis) | Data Analysis | SQL, Excel, Python |

See the [live site](https://sanjibsamadder.github.io) for the full gallery.

## Contact

- **Email:** [skilled.sanjib@gmail.com](mailto:skilled.sanjib@gmail.com)
- **GitHub:** [@sanjibSamadder](https://github.com/sanjibSamadder)
- **LinkedIn:** [linkedin.com/in/sanjibsamadder](https://linkedin.com/in/sanjibsamadder/)

## License

© 2026 Sanjib Samadder. All rights reserved.

The code is shared for reference. Please don't copy the content, project write-ups or personal branding. If you'd like to reuse the layout as a template for your own site, feel free to get in touch.

