# GQA Chinese Translation

This repository contains a Chinese LaTeX translation of the paper "GQA: Training Generalized Multi-Query Transformer Models from Multi-Head Checkpoints".

The paper studies how to uptrain existing multi-head attention language model checkpoints into multi-query attention models, and introduces grouped-query attention as a better trade-off between inference speed and model quality.

## Repository Layout

- `main.tex`: Main paper source, including the Chinese title, abstract, body, and appendix.
- `custom_commands.tex`: LaTeX macros used by the paper.
- `figures/`: Figure environments and translated captions.
- `tables/`: Table environments and translated captions.
- `custom.bib`: Bibliography database.
- `emnlp2023.sty`: Paper template style file.

## Build

This project is built with XeLaTeX. Chinese typesetting depends on `xeCJK` and the local Chinese font configuration used in `main.tex`.

```bash
xelatex -halt-on-error -interaction=nonstopmode -file-line-error main.tex
bibtex main
xelatex -halt-on-error -interaction=nonstopmode -file-line-error main.tex
xelatex -halt-on-error -interaction=nonstopmode -file-line-error main.tex
```

The generated PDF is `main.pdf`.

## Translation Notes

- The original LaTeX structure, citations, labels, equations, and bibliography are preserved.
- Author names, model names, dataset names, and common technical terms remain in English.
- The body text, section titles, figure captions, and table captions are translated into Chinese.
- Table data and plotting code are unchanged.

## License and Citation

This repository only provides a Chinese translation and organized LaTeX source. The original paper content, figures, tables, and references belong to their original authors. Please cite the original paper when using or referencing the research content.
