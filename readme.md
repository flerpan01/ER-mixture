# README

>The code in this repo was used to generate reults for this paper: [paper-title](https://doi.org)

## Project summary

Anthropogenic chemicals are wide spread in society and many of these compounds can mimic and disrupt the endocrine system, being classified as endocrine disrupting chemicals.

This project aims to evaluate the potential endocrine disruption effect of real-world personalized chemical mixtures on estrogen receptor (ER) activity, based on the blood serum sample from participants of the Swedish Västerbotten intervention programme (VIP). The defined concentrations of 24 chlorinated, brominated and fluorinated persistent organic pollutants (POP) were measured and 16 component-based personalized chemical mixtures were reconstructed using an automated liquid handling system. The mixtures and their individual chemicals were tested in an optimized and scaled-up 384-well plate high throughput screening (HTS) version of the OECD test guideline No.455 protocol for endocrine disruption, using the VM7 cell line as an ER reporter system.

## Project structure

```sh
proj/
|-- code
|   `-- analysis.R
|-- misc
|   |-- mixtures__rmix.xlsx
|   `-- single_cmpd_rmix.xlsx
`-- readme.md
```

## Code

The code based on [POP-screening project](https://github.com/flerpan01/POP-screening), but modified to different input data.

The script is self-sufficient and will generate the needed folders. Plots will be generated inside `img` and statistical tables inside `data`.

>To reproduce the results, run the code below (modify `DIR`)

```sh
DIR="path/to/project-directory"
cd $DIR

Rscript code/analysis.R
```

---

>This project was made by the [Karlsson Laboratory](https://karlssonlab.se/) at Stockholm University, Sweden
