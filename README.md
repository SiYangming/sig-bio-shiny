# sig-bio-shiny

<!-- badges: start -->
  [![Lifecycle: experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
  [![Build Status](https://travis-ci.org/sk-sahu/sig-bio-shiny.svg?branch=master)](https://travis-ci.org/sk-sahu/sig-bio-shiny)
  [![CircleCI](https://circleci.com/gh/sk-sahu/sig-bio-shiny.svg?style=svg)](https://circleci.com/gh/sk-sahu/sig-bio-shiny)
  [![GitHub release (latest by date)](https://img.shields.io/github/v/release/sk-sahu/sig-bio-shiny)](https://github.com/sk-sahu/sig-bio-shiny/releases)
  [![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/sudosk/sig-bio-shiny)](https://hub.docker.com/repository/docker/sudosk/sig-bio-shiny/builds)
<!-- badges: end -->

R shiny application for doing significant biology on a set of genes. 

**Significant Biology** is an important step of any high-throughput sequence analysis. Once you maped and/or assembled sequenced reads followed by feature(gene/isoform) quantification and/or diffrential analysis you will end up with set of genes. Quickly explore those genes from diffrent aspect what gives an idea about the Biology they involved in. Here comes this **SigBio** Shiny application. This is platform where with a set of genes you can do **Gene Ontology (GO), KEGG Pathway, Enrichment, Annotation and many things (will be discussed soon).**

1. [Requirement](#requirements)
2. [Download](#download)
4. [Run the shiny app](#run-the-shiny-app)

## Requirements
R >= 3.5

## Download
First you need to install the SigBio package which have the APIs required for most functionality in the app.
```r
if (!require(remotes)) { install.packages("remotes") }
  remotes::install_github("sk-sahu/sig-bio-shiny", 
                          ref = "v0.2.0")
```

Download a specific version of the app using wget from terminal
```bash
wget https://raw.githubusercontent.com/sk-sahu/sig-bio-shiny/v0.2.0/app.R -O sig-bio-shiny-app-v0.2.0.R
```
On the first time of running This will download and install all the required dependency.

## Run the shiny app
From your terminal
```bash
Rscript sig-bio-shiny-app-v0.2.0.R
```
Access the app in your browser with output URL.

### Run with docker
```bash
docker pull sudosk/sig-bio-shiny:v0.2.0
docker run --user shiny --rm -p 80:3838 sudosk/sig-bio-shiny:v0.2.0
```
Accessed app in a browser at http://127.0.0.1
