Mr. Fraction's Factory

An interactive, dyslexia-friendly tool for teaching fractions, decimals, and percentages to middle school students. Everything lives in a single self-contained HTML file styled as a factory that produces fractions, with Mr. Fraction guiding students through every step.

🔗 Live site: jtaylor-cloud.github.io/Mr.FractionFactory

## What it does
Students enter through a loading screen (Mr. Fraction dancing), land on the factory home page, and pick a station. Each station teaches the same numbers from a different angle — fraction, decimal, and percent — so students stop seeing them as separate topics.

## Station -- Name -- What Students Do

01 -- Job Training -- A guided, multi-step lesson on what fractions are and how to operate on them, with Mr. Fraction dialogue that names what students are noticing and surfaces the why. Includes the multiplication area-grid model.

02 -- Simplifier -- Reduce fractions to lowest terms with a full Euclidean-algorithm engine, animated step reveals, and canvas pie charts.

03 -- Operations -- Add, subtract, multiply, and divide fractions with visual area models, sign toggles, LCD coaching, and division-bracket arrows.

04 -- Converter --Turn fractions into decimals and percentages with pie charts, number lines, and percent bars shown side by side.

05 -- Factory Floor -- Seven randomized, gamified challenges across three difficulty tiers. Ships only on 100% correctness, with "Try Again" on every challenge and a Certificate of Completion at the end.

Mr. Fraction appears at the bottom of every page except the home page.

Design priorities

Dyslexia-friendly first. Atkinson Hyperlegible throughout, generous spacing, high contrast, and plain-language explanations.
Dialogue does real work. Mr. Fraction names the pattern a student is seeing rather than just cheering them on, and consistently ties fractions, decimals, and percents back together.
Visuals are the lesson, not decoration. The Station 01 lesson grid deliberately mirrors the Station 03 operations tool, so students practice on the exact visual they were taught with.
Pedagogical accuracy is non-negotiable. Example: the multiplication area model uses a dynamic multi-unit grid so improper fractions are handled correctly, instead of falsely teaching that products are always smaller.

Tech

Single self-contained HTML file — no build tools, no frameworks, no dependencies to install.
Plain HTML / CSS / JavaScript.
Google Fonts CDN for Atkinson Hyperlegible (plus Black Han Sans and Libre Baskerville for display/certificate text).
Pointer-events drag-and-drop for cross-device support (mouse, touch, and Chromebook).
Deployed via GitHub Pages.

## Running it

Just open mr_fraction_factory.html in a browser — or visit the live site above. No server or setup required.

Image assets
All images are referenced by their exact filenames and must live in the repo root alongside the HTML:

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

Don't rename these or change their extensions — the file references them directly, and there are no fallbacks.

## License

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material

Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made
- **NonCommercial** — You may not use the material for commercial purposes
- **ShareAlike** — If you remix or build upon this material, you must distribute your contributions under the same license

[![CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

*Built with ❤️ for middle schoolers who just need to see the fraction.*
