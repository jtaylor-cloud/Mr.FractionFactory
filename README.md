# Mr. Fraction's Factory

An interactive, dyslexia-friendly tool for teaching fractions, decimals, and percentages to middle school students. Everything lives in a single self-contained HTML file styled as a factory that *produces fractions*, with Mr. Fraction guiding students through every step.

🔗 **Live site:** [jtaylor-cloud.github.io/Mr.FractionFactory](https://jtaylor-cloud.github.io/Mr.FractionFactory/)

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

## What it does

Students enter through a loading screen (Mr. Fraction dancing), land on the factory home page, and pick a station. Each station teaches the same numbers from a different angle — fraction, decimal, and percent — so students stop seeing them as separate topics.

| Station | Name | What students do |
|--------|------|------------------|
| 01 | **Job Training** | Two bays and a workshop. **Bay A — What Fractions Are** (10 steps): what a fraction is, what each number controls, equivalence, the number line, negatives, and why some decimals never end. **Bay B — Working With Fractions** (7 steps): mixed numbers, the GCF, adding and subtracting, percents, multiplying, and dividing. **Division Workshop** (4 steps, optional): place value as an exchange, dealing out into groups, and what "bring down a zero" really means. Students pick a door and can switch at any time. |
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
4. **The Hundred Mould** — percent as a denominator, not an operation
5. Multiplying Fractions — read the grid
6. **The Measuring Line** — division as measurement ("how many of these fit inside that?"), then why you flip

**Division Workshop** *(optional, reachable from any machine that needs it)*

1. **The Exchange Counter** — place value as an exchange. Break one whole into ten tenths, a tenth into ten hundredths, and watch the total value refuse to move
2. **Dealing Out** — deal items round-robin into groups, one round at a time. The number of complete rounds *is* the quotient; whatever cannot make one more round is the remainder
3. **Exchange the Leftovers** — the leftovers sit in the Ones column, get exchanged for tenths, and get dealt again

Deliberately outside both bays. A confident student never opens it; a struggling one reaches it from a **🔧 Shaky on division?** button inside the Dividing Machine, the Repackaging Line, the Measuring Line, or Station 04's Remainder Belt. It remembers which bay and step they came from — or which station — and hands them back there when they finish.

The workshop never says "multiply the remainder by ten". That framing is why the step does not land. It is an **exchange** — the same amount in finer pieces, one column to the right — and the phrase "bring down a zero" is introduced last, as the name for what the student has just done.

## One rule, three forms

The site's spine is that a fraction, its decimal, and its percent are one number, and that a single rule governs all three.

- **A fraction is a division.** The bar means divide. Run it and you get the decimal.
- **A percent is a denominator.** "Per cent" means *per hundred*, so a percent is the same fraction re-cut into a mould of 100 — not a calculation.
- **The same rule decides both.** A denominator built only from **2s and 5s** gives a decimal that stops, because 10 = 2 × 5. And **100 = 2 × 2 × 5 × 5**, so that identical rule decides whether the percent is clean. A fraction with a repeating decimal has a repeating percent for exactly the same reason — verified across every fraction with a denominator below 100.

Repeating decimals then run through the whole site rather than sitting in one lesson:

- **Correct notation everywhere.** A repeating decimal renders with a proper vinculum, and the bar covers only the digits that actually repeat.
- **Station 01** teaches *that* it happens and the 2s-and-5s rule that predicts it.
- **Station 04's Remainder Belt** teaches *why* it is unavoidable. A crate carries each remainder to a stamper; if the remainder is not zero, a return chute sends it back. On a repeating decimal the machine physically cannot stop — the student has to shut it down. It prints the real long division as it goes.
- **Challenge 9 (Stamp the Bar)** assesses the skill students actually fail: placing the bar over exactly one period, starting where the repeat truly starts.

## What Mr. Fraction does

The speech bubble is not decoration. It carries three jobs the screen cannot.

**It walks through simplifications the screen performs silently.** Station 03 reduces every answer inside its render function, so a student who works out `6/8` is shown `3/4` with no account of the jump. Now:

> You worked out **12/18**, but the screen shows **2/3**. Here is the route: 12/18 ÷ 2 → **6/9**, then 6/9 ÷ 3 → **2/3**. Or in one go — both divide by **6**.

Composite factors are staged, because a student who cannot spot 6 can usually spot 2. Top-heavy results get the mixed number as well. Already-simple answers produce no dialogue at all. This fires on all four operations, in the Simplifier, and on a wrong lowest-terms answer in Challenge 4.

**It adapts to whether the student has done the Division Workshop.** Before: *"This one is really a division question underneath — the workshop is three short steps."* After: the workshop's own language everywhere, so the Remainder Belt becomes *"every line in that log is one workshop round: deal what you can, exchange the leftover for ten, go again."* Two wrong answers on anything division-shaped from someone who has never opened it, and he offers it with a working button.

**It occasionally makes a joke.** Fifteen of them, rationed by three rules: never while the student is on a wrong streak, never in the middle of an explanation, and never within four exchanges of the last one. A joke landing on someone who is stuck reads as being laughed at.

> *"I asked a repeating decimal when it would be finished. Still waiting."*

## Design priorities

- **Dyslexia-friendly first.** [Atkinson Hyperlegible](https://fonts.google.com/specimen/Atkinson+Hyperlegible) throughout, generous spacing, high contrast, left-aligned body text, and plain-language explanations.
- **Let it fail first.** The Mixing Line refuses to add 1/4 and 1/6 and shows the mismatched pieces, so the common denominator is discovered as a solution to a problem the student just hit. The Dividing Machine makes you call it before it runs.
- **Discovery is withheld, not announced.** The Sevenths Wheel will not tell you the pattern until you have checked all six.
- **Dialogue does real work.** Mr. Fraction runs on a small learner model built only from what a student actually does — which fractions they explore, how many terminating versus repeating cases they meet, their prediction accuracy, whether they have been through the workshop. Probes are computed from their own history. After repeated wrong answers he narrows the question, then states the rule outright rather than asking a fifth riddle.
- **Pedagogical accuracy is non-negotiable.** The multiplication area model uses a dynamic multi-unit grid so improper fractions are handled correctly. There is exactly one long-division implementation in the file, shared by every machine that needs it.

## Accessibility notes

- The repeating-decimal bar is drawn with a CSS `border-top`, **not** the Unicode combining overline (U+0305), which renders inconsistently across fonts and is mangled by screen readers. The visual form is `aria-hidden`, with a spoken form supplied alongside.
- Interactive controls prefer **▲▼ buttons over drag-and-drop** for touch and Chromebook reliability. Challenge 1 still offers drag, implemented with pointer events so it works with mouse and touch alike.
- Colour is never the only signal: fills and cut lines differ in lightness as well as hue.

## Mobile

- Station 03's controls stack below 700px — the label moves above the slider, which previously left the slider about 3px wide on a 320px phone.
- Every numeric field opens the right keypad: `inputmode="numeric"` for whole numbers, `inputmode="decimal"` for the decimal and percent boxes.
- Station 03 gained typed number entry for whole numbers, denominator and numerator, so nobody has to tap a 5px cell.
- Page gutters tighten below 600px, and `@media (pointer: coarse)` puts a 40px minimum on small controls.

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
