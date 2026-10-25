# Quiizy Campus Assistant: Research Paper

The LaTeX source of the research paper *An LLM-Based Bilingual Campus
Assistant for Academic Service Access via RAG and Quiizy Integration: Design,
Implementation, Cloud Deployment and Evaluation in a Central African
University* (March 2026).

The paper describes a web-based campus AI assistant that answers students'
academic and administrative questions in English and French. It uses a large
language model with a retrieval-augmented generation (RAG) pipeline, is
designed to integrate with Quiizy (the university's multiple-choice assessment
platform), and is deployed on AWS. The work follows the Nunamaker research
methodology and is evaluated with a cognitive walkthrough and a student survey
based on the Technology Acceptance Model.

**Authors:** Moutcheu Somo Gift Anderson, Abena Alex Nelson Ryan, Foning
Lackmata Luc-Xavier, Fotsing Kengne Weber, Chengho Fongang Marie Louise,
Kouetche Simo Yann and Takam Sokoudjo Ismael Ulrich.
**Supervisor:** Dr.-Ing. Philippe Tamla.

## Read the paper

The compiled paper is committed as [`main.pdf`](main.pdf). Open it directly on
GitHub, or download it.

## Build it yourself

You need a TeX distribution (TeX Live or MiKTeX) with `pdflatex`, `biber` and
`makeglossaries`, plus Python with [Pygments](https://pygments.org), which the
`minted` package uses for code listings.

```bash
git clone https://github.com/NinjaShadowBoy/quizzy-reasearch-paper.git
cd quizzy-reasearch-paper
pip install Pygments

pdflatex -shell-escape main.tex
biber main
makeglossaries main
pdflatex -shell-escape main.tex
pdflatex -shell-escape main.tex
```

`-shell-escape` is required by `minted`. If you use
[latexmk](https://ctan.org/pkg/latexmk), `latexmk -pdf -shell-escape main.tex`
runs all the passes for you.

## Layout

```
main.tex                          the paper
assets/include/elaboration.sty    page layout, title page and package setup
assets/include/bibliographie.bib  references
assets/include/glossar.tex        glossary entries
images/                           diagrams (UML, MVC, components) and demo recordings
```
