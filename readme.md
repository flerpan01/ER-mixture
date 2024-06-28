# README

>The code in this repo was used to generate reults for this paper: [Effects of personalized chemical mixtures on an estrogen receptor activity based on high throughput screening assay, 2024, some-journal](https://doi.org)

## Project summary

Anthropogenic chemicals are wide spread in society and many of these compounds can mimic and disrupt the endocrine system, being classified as endocrine disrupting chemicals.

In this project, we evaluate the potential endocrine disruption effect of real-world personalized chemical mixtures on estrogen receptor (ER) activity, based on the blood serum sample from participants of the Swedish Västerbotten intervention programme (VIP). The defined concentrations of 24 chlorinated, brominated and fluorinated persistent organic pollutants (POP) were measured and 16 component-based personalized chemical mixtures were reconstructed using an automated liquid handling system. The mixtures and their individual chemicals were tested in an optimized and scaled-up 384-well plate high throughput screening (HTS) version of the OECD test guideline No.455 protocol for endocrine disruption, using the VM7 cell line as an ER reporter system.

## Project structure

The dataset is composed two excel documents (`mixtures__rmix.xlsx` and `single_cmpd_rmix.xlsx`) with the columns: (1) `cmpd` the name of the compounds used or the number of the individual mixture, (2) `treat` the specific concentration of each compound or mixture, (3) `n` the experimental batch and (4) `RLT` the output measurement. The excel documents are further divided three sheets with (1) agonist, (2) antagonist and (3) viability. 

```
project/
|-- code
|   └-- analysis.R
|-- doc
|   |-- mixtures__rmix.xlsx				dataset
|   └-- single_cmpd_rmix.xlsx			dataset
└-- readme.md
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
