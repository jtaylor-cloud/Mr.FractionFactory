# 🏭 Mr. Fraction Factory

**An interactive, dyslexia-friendly fraction learning website for middle school students**

Live site → `https://jtaylor-cloud.github.io/Mr.FractionFactory/`

---

## What It Is

Mr. Fraction Factory is a single-file static HTML learning tool built for middle schoolers who are just getting comfortable with fractions. It runs entirely in the browser — no server, no login, no tracking. Just open the page and start learning.

The site is structured like a factory where Mr. Fraction (your animated guide) runs the machines that build, simplify, operate on, and convert fractions. Every section is self-contained and can be used standalone or as part of a lesson sequence.

---

## What's Inside

| Section | What Students Do |
|---|---|
| **Lesson** | Read and interact with a step-by-step explanation of what fractions are, what numerators and denominators mean, and how fractions, decimals, and percentages are all the same thing |
| **Simplify** | Enter any fraction, see its factors highlighted, find the GCF, and watch the fraction reduce step by step |
| **Operate** | Build two fractions with sliders, choose +, −, ×, or ÷, and see a color-coded visual bar or grid showing exactly what the operation means |
| **Convert** | Slide between fraction, decimal, and percentage representations simultaneously — all three update live |

Mr. Fraction appears at the bottom of every section page with rotating dialogue that ties the math together. He doesn't just cheer — he asks questions, makes connections, and challenges students to explain what they see.

---

## File Structure

```
/
├── mr_fraction_factory.html     ← The entire app (one file)
├── Mr__Fraction_GIF.gif         ← Loading screen animation
├── Mr__Fraction_Front.png       ← Home page hero image
├── Mr__Fraction_Left_Side.png   ← Used in lesson cards
├── Mr__Fraction_Right_Side.png  ← Used in lesson cards
├── Mr__Fraction_Back.png        ← Used in factory scenes
├── Mr__Fraction_Ladder.png      ← Decorative / section headers
├── Pizza.png                    ← Interactive pizza in the lesson
├── Pie.png                      ← Used in the converter section
├── Gear.png                     ← Factory theme decoration
└── README.md                    ← This file
```

All images are referenced as relative paths — keep them in the same directory as the HTML file.

---

## Hosting on GitHub Pages

1. Create a new GitHub repository (public)
2. Upload `mr_fraction_factory.html` and all `.png` / `.gif` files to the root of the repo
3. Go to **Settings → Pages**
4. Under **Source**, select `Deploy from a branch` → `main` → `/ (root)`
5. Click **Save**
6. Your site will be live at `https://<your-username>.github.io/<repo-name>/mr_fraction_factory.html` within a minute or two

If you want the site to load at the root URL without the filename, rename `mr_fraction_factory.html` to `index.html`.

---

## Design Decisions

**Dyslexia-Friendly**
The site uses [Atkinson Hyperlegible](https://brailleinstitute.org/freefont), a font designed specifically for readers with low vision and dyslexia. Font sizes are large, line height is generous, and color is never the only way information is conveyed.

**No Base64 Images**
Images are loaded as external `.png` and `.gif` files. This keeps the HTML file lightweight and readable, and makes it easy to swap or update character art without touching the code.

**Single File (Mostly)**
All CSS and JavaScript live inside `mr_fraction_factory.html`. The only external dependencies are the Google Fonts CDN (for Atkinson Hyperlegible) and the image files. The site works offline if you pre-load the font or remove the Google Fonts link.

**Factory Theme**
The warm cream-and-brown palette (`#f5ede0`, `#2c2214`, `#c8b89a`) and gear/conveyor-belt visual language carry through every section. Mr. Fraction's dialogue changes dynamically based on what the student is doing — he's not a static decoration.

---

## Accessibility Notes

- Minimum font size is 13px; most body text is 15–16px
- All interactive controls (sliders, buttons) have visible focus states
- Color contrast meets WCAG AA for all text on backgrounds
- The pizza and pie visuals include `alt` text
- Mr. Fraction's speech is rendered as readable text, not just decorative

---

## Customizing

**Swap the character art** — replace any `.png` file with your own, keeping the same filename. The HTML references filenames directly, so no code changes needed.

**Change dialogue** — search for the `mrDialogues` array in the HTML source. Each section has its own rotating list of quotes. Add, remove, or edit freely.

**Add a new section** — each section is a `<section id="phase-X">` block. Copy an existing one, update the nav button in the home screen, and wire it up in the `showPhase()` function.

---

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). No IE support — range input styling and CSS Grid are both used extensively.

---

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
