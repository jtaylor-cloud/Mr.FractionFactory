# Mr. Fraction's Factory

An interactive, dyslexia-friendly tool for teaching fractions, decimals, and percentages to middle school students. Everything lives in a single self-contained HTML file styled as a factory that *produces fractions*, with Mr. Fraction guiding students through every step.

🔗 **Live site:** [jtaylor-cloud.github.io/Mr.FractionFactory](https://jtaylor-cloud.github.io/Mr.FractionFactory/)

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

## What it does

Students enter through a loading screen (Mr. Fraction dancing), land on the factory home page, and pick a station. Each station teaches the same numbers from a different angle — fraction, decimal, and percent — so students stop seeing them as separate topics.

| Station | Name | What students do |
|--------|------|------------------|
| 01 | **Job Training** | Two training bays. **Bay A — What Fractions Are** (10 steps) covers what a fraction is, what each number controls, equivalence, the number line, negatives, and why some decimals never end. **Bay B — Working With Fractions** (6 steps) covers mixed numbers, the GCF, adding and subtracting, multiplying, and dividing. Students pick a bay and can switch at any time. |
| 02 | **Simplifier** | Reduce fractions to lowest terms with a full Euclidean-algorithm engine, animated step reveals, and canvas pie charts. |
| 03 | **Operations** | Add, subtract, multiply, and divide fractions with visual area models, sign toggles, LCD coaching, and division-bracket arrows. |
| 04 | **Converter** | Change any value — fraction, decimal, or percent — and watch the others follow, with pie charts, number lines and percent bars side by side. Includes **The Remainder Belt**, a working long-division machine. |
| 05 | **Assessment Bay** | Nine randomized, gamified challenges across four difficulty tiers. Ships only on 100% correctness, with "Try Again" on every challenge and a Certificate of Completion at the end. |

Mr. Fraction appears at the bottom of every page except the home page.

## Inside Job Training

**Bay A — What Fractions Are**

1. What is a Fraction? — eat a drawn pizza slice by slice; eaten and remaining fractions move together
2. The Two Numbers — a live model where the denominator re-cuts the whole and the numerator only fills it
3. Types of Fractions
4. Equivalent Fractions
5. Fractions on a Number Line
6. **Below Zero** — negative fractions as mirror images, including the ordering trap (−3/4 < −1/2)
7. **The Dividing Machine** — predict "clean cut or endless loop", then watch real long division settle it
8. **The Sevenths Wheel** — discover that all six sevenths are the same six digits, rotated
9. Fractions in Real Life

**Bay B — Working With Fractions**

1. **The Repackaging Line** — improper ↔ mixed numbers; the leftover pieces *are* the remainder
2. Finding the GCF — the Euclidean machine
3. **The Mixing Line** — adding and subtracting. Combining fails first, which is how the common denominator earns its existence
4. Multiplying Fractions — read the grid
5. **The Measuring Line** — division as measurement ("how many of these fit inside that?"), then why you flip

## The repeating-decimal thread

Repeating decimals run through the whole site rather than sitting in one lesson:

- **Correct notation everywhere.** A repeating decimal renders with a proper vinculum — `0.416` with a bar over the 6, not `0.4167`. The bar covers only the digits that actually repeat.
- **Station 01** teaches *that* it happens and the rule that predicts it: denominators built only from 2s and 5s terminate, because 10 = 2 × 5.
- **Station 04's Remainder Belt** teaches *why* it is unavoidable. A crate carries each remainder to a stamper; if the remainder is not zero, a return chute sends it back and the machine runs again. On a repeating decimal it physically cannot stop — the student has to shut it down. It prints the real long division as it goes.
- **Challenge 9 (Stamp the Bar)** assesses the skill students actually fail: placing the bar over exactly one period, starting where the repeat truly starts.

## Design priorities

- **Dyslexia-friendly first.** [Atkinson Hyperlegible](https://fonts.google.com/specimen/Atkinson+Hyperlegible) throughout, generous spacing, high contrast, left-aligned body text, and plain-language explanations.
- **Dialogue does real work.** Mr. Fraction runs on a small learner model built only from what a student actually does — which fractions they explore, how many terminating versus repeating cases they meet, their prediction accuracy. Lines are chosen to fit where they are, and probes are computed from their own history ("Everything you have tried has stopped neatly. Try 1/6 — what will it do?"). After repeated wrong answers he narrows the question, then states the rule outright rather than asking a fifth riddle.
- **Discovery is withheld, not announced.** The Sevenths Wheel will not tell you the pattern until you have checked all six. The Dividing Machine makes you call it before it runs.
- **Visuals are the lesson, not decoration.** The Station 01 lesson grid deliberately mirrors the Station 03 operations tool, so students practice on the exact visual they were taught with.
- **Pedagogical accuracy is non-negotiable.** The multiplication area model uses a dynamic multi-unit grid so improper fractions are handled correctly, instead of falsely teaching that products are always smaller. There is exactly one long-division implementation in the file, shared by every machine that needs it.

## Accessibility notes

- The repeating-decimal bar is drawn with a CSS `border-top`, **not** the Unicode combining overline (U+0305), which renders inconsistently across fonts and is mangled by screen readers. The visual form is `aria-hidden`, with a spoken form supplied alongside ("zero point four one, six repeating").
- Interactive controls prefer **▲▼ buttons over drag-and-drop** for touch and Chromebook reliability. Challenge 1 still offers drag, implemented with pointer events so it works with mouse and touch alike.
- Colour is never the only signal: cut lines, fills and stripes are chosen to differ in lightness as well as hue.

## Tech

- **Single self-contained HTML file** — no build tools, no frameworks, no dependencies to install. One `<style>` block, one `<script>` block, zero external JavaScript.
- Plain HTML / CSS / JavaScript.
- [Google Fonts CDN](https://fonts.google.com) for Atkinson Hyperlegible (plus Black Han Sans and Libre Baskerville for display/certificate text) — the only network request the page makes.
- Deployed via GitHub Pages.

## Running it

Just open `index.html` in a browser — or visit the live site above. No server or setup required.

### Image assets

All images are referenced by their exact filenames and must live in the repo root alongside `index.html`:

```
Mr__Fraction_Front.png
Mr__Fraction_Back.png
Mr__Fraction_Left_Side.png
Mr__Fraction_Right_Side.png
Mr__Fraction_Ladder.png
Mr__Fraction_Factory.png
Mr__Fraction_GIF.gif
Gear.png
Pie.png
Pizza.png
```

Don't rename these or change their extensions — the file references them directly, and there are no fallbacks.

### Updating the site

Replace `index.html` in the repo root and push. GitHub Pages caches aggressively at this file size, so hard-refresh (Ctrl/Cmd + Shift + R) before deciding something is broken.

## License

[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You're free to share and adapt this for non-commercial use, with attribution, as long as you license your version the same way.

[![CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

*Built with ❤️ for middle schoolers who just need to see the fraction.*
