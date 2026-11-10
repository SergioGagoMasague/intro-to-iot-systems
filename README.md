# Introduction to IoT Systems

*Building connected devices from the breadboard up* — an open textbook for a hands-on IoT systems course built around an ESP32 team kit.

- Text and figures: [CC BY 4.0](LICENSE-TEXT.md)
- Code: [MIT](LICENSE-CODE.md)

## Building the book

1. Install [Quarto](https://quarto.org/docs/get-started/) (1.5 or later). Typst, used for the PDF, ships with Quarto.
2. Install the Quarto extension for VS Code (optional, for live preview).
3. From this folder:

```bash
quarto preview            # live-reloading website while you write
quarto render             # website (_book/) and PDF
quarto render --to html   # website only
```

## Repository layout

```
_quarto.yml                 book configuration (chapter order, formats)
index.qmd                   preface
how-to-use.qmd              using the book with the kit
part1-foundations/ …        core chapters (Parts I–VI)
part7-lab-companion/        Lab Companion (versioned per term)
appendices/                 kit reference, toolchain, troubleshooting, glossary
images/                     figures (SVG preferred)
code/                       example sketches referenced by chapters
references.bib              bibliography
CHAPTER_TEMPLATE.qmd        copy this to start a new chapter
```

## Writing conventions

- Course-neutral wording: "IoT@UCI" for the kit, "this course" in prose. No course numbers.
- Code uses the `iot_*` helpers and `IoTPins::` names from `iot_pins.h`.
- Every chapter follows `CHAPTER_TEMPLATE.qmd`.
- Advanced material goes in `::: {.callout-note title="Advanced track"}` blocks.
- Instructor-only material (solutions, rubrics, polls) lives in a separate private repository, never here.

## Publishing

- **Website:** GitHub Pages via `quarto publish gh-pages`, or a GitHub Action.
- **Citable releases:** connect the repository to Zenodo; each tagged release (for example `v2027.1`) receives a DOI.
