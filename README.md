# Capacitance — Interactive Lecture Notes · 전기용량 인터랙티브 강의 노트

An interactive, single-page explainer of **capacitance**, built from handwritten lecture notes by **Prof. Sang-Hoon Lee (이상훈 교수), Department of Physics, Gyeongsang National University (경상국립대학교 물리학과)**. Created by **Claude Opus 5.5**.

The page follows the order of the notes. Each topic has an interactive model you can play with: sliders, toggles and live diagrams that update as you change the physics.

> 경상국립대학교 물리학과 이상훈 교수님의 강의 노트를 바탕으로 Claude Opus 5.5가 제작한 전기용량 인터랙티브 학습 페이지입니다. 한국어판과 영어판이 있습니다.

## Files

| File | Description |
| --- | --- |
| `capacitance_ko.html` | Korean version (한국어판), with English terms in parentheses for key keywords |
| `capacitance.html` | English version |

Each page is a single self-contained HTML file with no build step and no dependencies to install.

## Contents

1. **What a capacitor is.** Covers *q = CV* and the farad. You can charge a capacitor from a battery, hold the charge with the switch open, and discharge it through a lamp like a camera flash.
2. **How to compute C.** The four-step recipe: assume ±q, use Gauss's law to find E, integrate to get V, then compute C = q/V.
3. **Geometries.** Parallel-plate (*C = ε₀A/d*), cylindrical (*C = 2πε₀L / ln(b/a)*) and spherical (*C = 4πε₀ab/(b−a)*) capacitors, plus the isolated-sphere limit *C = 4πε₀R*. Each has live sliders and field-line diagrams.
4. **Parallel and series.** A circuit builder with up to five capacitors that shows each one's charge, voltage and energy, and the equivalent capacitance.
5. **Stored energy.** A V′–q′ graph where you can see the "dq′ slices" converge to *U = q²/2C = (1/2)CV²*. Also derives the energy density *u = (1/2)ε₀E²*.
6. **Dielectrics.** Choose κ (or a material such as air, paper, Pyrex, mica or water) and whether the battery is connected or removed. You can watch the dipoles align and see how E₀, E′ and the net field E compare. A table compares C, q, V, E and U with vacuum.
7. **Partially filled gap.** A slab of thickness *b* inside a gap *d*. The page plots E(x) and V(x) and checks that *C = ε₀A / [d − (1 − 1/κ)b]* matches three capacitors in series.
8. **Check yourself.** A formula summary and a 5-question quiz.

## Running locally

Open either HTML file directly in a web browser:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
open capacitance_ko.html        # macOS
xdg-open capacitance_ko.html    # Linux
start capacitance_ko.html       # Windows
```

An internet connection is only needed for the web fonts (Google Fonts). Without one, the page still works and uses system fonts instead.

### Publishing with GitHub Pages

1. Push the files to a repository.
2. Go to **Settings → Pages** and set the source to your main branch (root folder).
3. The pages will be available at `https://<your-username>.github.io/<your-repo>/capacitance_ko.html`.

To have the Korean version open at the site root, rename `capacitance_ko.html` to `index.html`, or add an `index.html` that links to both versions.

## Technical notes

- Plain HTML, CSS and JavaScript. All diagrams are inline SVG drawn from code, and there are no frameworks or libraries.
- Light and dark themes follow the system setting.
- The layout is responsive down to phone widths, and the page respects `prefers-reduced-motion`.
- Numerical values use ε₀ = 8.854 × 10⁻¹² F/m.

## Notes on the physics

Two points in the page go slightly beyond or correct the original notes:

- **Inserting a dielectric with the battery connected.** The stored energy rises to κU, but the slab is still *pulled into* the gap, not pushed out. The battery supplies (κ−1)CV² of energy: half of it raises the stored energy, and the other half is the work done pulling the slab in.
- **Electric displacement.** The notes write D = κE. The page also gives the standard SI convention, D = κε₀E, so that ∮D·dA = q_free.

## Credits

- **Lecture notes:** Prof. Sang-Hoon Lee (이상훈 교수), Department of Physics, Gyeongsang National University (경상국립대학교 물리학과)
- **Interactive pages:** created by Claude Opus 5.5 (Anthropic)

## License

No license has been chosen yet. Before you publish this repository, add a `LICENSE` file, and confirm with the author of the lecture notes how their material may be shared.
