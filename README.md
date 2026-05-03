# n-Ball Explorer

**An interactive, beautiful web demo exploring the volume of n-dimensional balls** — inspired by 3Blue1Brown’s video *"The most beautiful formula not enough people understand"* (https://www.youtube.com/watch?v=fsLh-NYhOoU).

## What It Teaches

This single-page app makes the elegant mathematics of higher-dimensional spheres tangible and fun:

- **Live Formula Explorer**: Adjust dimension *n* (continuous 1–20) and radius *r*. Watch the exact closed-form volume  
  **Vₙ(r) = π^{n/2} / Γ(n/2 + 1) × rⁿ**  
  and surface measure update in real time with beautiful KaTeX rendering. Hover parts of the formula for geometric explanations.

- **Interactive Volume Grid & Slicing**: See the Archimedes-style recurrence in action.  
  **Vₙ(r) = ∫_{-r}^r V_{n-2}(√(r² − x²)) dx**  
  Move your mouse (or slider) across a live cross-section. The app computes the infinitesimal contribution from each slice and shows how the lower-dimensional volume builds the higher one.

- **Dimension Sweep Plot**: A smooth Chart.js plot of unit-ball volume Vₙ(1) and surface S_{n−1}(1) from n=1 to 30. The curve peaks around dimension 5–7 then plummets toward zero — exactly as the video reveals. Hover to sync with formula and preview.

- **High-Dimensional Intuition Demos**:
  - **Cube-with-Corner-Spheres Puzzle**: Watch how the central sphere “bursts out” of the hypercube as dimension increases (radius = √n − 1). This is the exact counter-intuitive example from the lecture.
  - **Volume Vanishes Animation**: See why a 100-dimensional unit ball has volume ~10^{-40} — almost all measure concentrates in an infinitesimally thin shell near the surface.

Everything runs **100% in the browser** (no backend). Perfect for GitHub Pages.

## Key Mathematical Highlights Covered

- Closed-form volume via Gamma function (extends factorial to reals)
- Recurrence relation from slicing (the “volume grid”)
- Archimedes’ cylinder insight generalized to any dimension
- Why volume maximizes near 5D and then collapses
- Surface area = dV/dr relationship
- Real-world relevance (machine learning embeddings, statistical mechanics, etc.)

## Tech Stack (GitHub Pages Ready)

- Pure HTML5 + Tailwind CSS (via Play CDN)
- Vanilla JavaScript
- KaTeX for gorgeous math rendering
- Chart.js for the interactive plot
- HTML5 `<canvas>` for all visualizations (no heavy Three.js)
- Fully responsive, dark 3Blue1Brown-inspired theme (deep navy + cyan glows)

## How to Run / Deploy

1. Clone or download this repo.
2. Open `index.html` directly in any modern browser (Chrome, Firefox, Safari, Edge).
3. Or push to GitHub and enable **GitHub Pages** (Settings → Pages → Deploy from `main` branch /root).

No build step, no npm install — just open the file.

## File Structure

```
n-ball-explorer/
├── index.html          # Complete self-contained app (all CSS/JS/KaTeX/Chart.js via CDN)
├── README.md           # This file
└── (no other assets needed)
```

## Credits & Inspiration

- **Grant Sanderson / 3Blue1Brown** — for the original lecture, manim animations, and making high-dimensional geometry feel magical.
- Video: [The most beautiful formula not enough people understand](https://www.youtube.com/watch?v=fsLh-NYhOoU)
- Formula: Standard result — volume of the n-ball of radius r is  
  **Vₙ(r) = π^{n/2} r^n / Γ(n/2 + 1)**

## Extending the Demo

- Add more dimensions or log-scale plots.
- Implement a true 3D WebGL slice using Three.js (easy fork).
- Add sound or confetti on “volume peak” or “burst”.
- Connect to real ML embedding visualizations.

Made with ❤️ for mathematical beauty. Fork it, play with it, and share what you discover!

---

*This project is 100% educational and open source. All formulas are numerically accurate within floating-point precision.*
