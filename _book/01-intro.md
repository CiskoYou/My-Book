# (PART) Get Started {-}

# Introduction

All chapters start with a first-level heading followed by your chapter title, like the line above. There should be only one first-level heading (`#`) per .Rmd file.

## Installation of R and Rstudio


All chapter sections start with a second-level (`##`) or higher heading followed by your section title, like the sections above and below here. You can have as many as you want within a chapter.

## Installation of R

To install R, we need to follow these basics instructions

### Windows:
- Go to the website of the <span style="color:orange">CRAN</span> (Comprehensive R Archive Network): [CRAN](https://cran.r-project.org/mirrors.html)
- Select a mirror close to your location.
- Click on the link "<span style="color:orange">Download R for Windows</span>".
- Click on "base" then on "<span style="color:orange">Download R x.x.x for Windows</span>" (where x.x.x is the latest version).
- Follow the installation instructions.

### Mac:
- Go to the website of the <span style="color:orange">CRAN</span>: [CRAN](https://cran.r-project.org/mirrors.html)
- Select a mirror close to your location.
- Click on the link "<span style="color:orange">Download R for (Mac) OS X</span>".
- Download the latest version "<span style="color:orange">R-x.x.x.pkg</span>" (where x.x.x is the latest version).
- Follow the installation instructions.

### Linux:
- Instructions vary by distribution. Check the <span style="color:orange">CRAN</span> for specifics to your distribution.

### Install RStudio:

- Go to the <span style="color:orange">RStudio</span> website: [RStudio](https://rstudio.com/products/rstudio/download/)
- Download the version suitable for your operating system (Windows, Mac, Linux).
- Follow the installation instructions.

## Intro to Rmarkdown

### Install `rmarkdown` from RStudio:

- Open <span style="color:orange">RStudio</span>.
- In the R console (typically at the bottom left), type:


```r
# Install from CRAN
install.packages('rmarkdown')

# Or if you want to test the development version,
# install from GitHub
if (!requireNamespace("devtools"))
  install.packages('devtools')
devtools::install_github('rstudio/rmarkdown')
```

- Press "Enter". This will install the `rmarkdown` package and its dependencies.

If you want to generate PDF output

1. You need to install **LaTeX**
2. Or you install TinyTeX (https://yihui.name/tinytex/), instead:

I will recommend the second option since it,s the easiest.


```r
install.packages('tinytex')
tinytex::install_tinytex()  # install TinyTeX
```

### Verifying the installation

In RStudio, go to `File` > `New File` > `R Markdown...`. If you can see a pop-up window allowing you to create a new R Markdown document, the installation was successful!

## First Rmardown code

R Markdown is a powerful tool for creating dynamic documents, presentations, and reports that combine narrative text with code and its output. It's especially popular in the data science community for its ability to integrate data analysis with documentation. The structure of an R Markdown document typically includes the following components:


1. A YAML header: The document begins with a YAML (Yet Another Markup Language) header, enclosed within `---` lines
2. A text: Normal text including elements like : headers, lists, links, etc.
3. A code chunk : R Markdown allows embedding R code chunks within the document. These chunks are enclosed in triple backticks (```) with {r} at the start to indicate they are R code. Within these chunks, you can write R code that can be executed to display results, graphs, and tables directly in the document

### YAML header

A YAML header is of the form 

```yaml
---
title: "Hello R Markdown"
author: "The big boss"
date: "2018-02-14"
output: html_document
---
```
