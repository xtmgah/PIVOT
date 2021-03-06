# PIVOT: Platform for Interactive analysis and Visualization Of Transcriptomics data

## About this package
This program is developed based on the Shiny framework, a set of R packages and a 
collection of scripts written by members of Junhyong Kim Lab at University of Pennsylvania. 
Its goal is to facilitate fast and interactive RNA-Seq data analysis and visualization. 
Current version of PIVOT supports routine RNA-Seq data analysis including normalization, 
differential expression analysis, dimension reduction, correlation analysis, clustering and 
classification. Users can complete workflows of DESeq2, monocle and scde package with
just a few button clicks. All analysis reports can be exported, and the program state can be
saved, loaded and shared.
  * See http://kim.bio.upenn.edu/software/pivot.shtml for more details.

## Installation
  * Main Program: Please copy and paste the following command to R console. 
  * Upgrading R and Rstudio to the latest version (R > 3.2, Rstudio > 1.0.0) is strongly recommended. 

```
# dependecies
install.packages("devtools")
library("devtools")
source("http://bioconductor.org/biocLite.R")  

# Install PIVOT
install_github("qinzhu/PIVOT")
install_github("qinzhu/PIVOT.launcher")
```
 * (Optional but strongly recommended) Dependencies:
   * For report generation, you need Pandoc: http://pandoc.org/installing.html
   * For PDF report generation, you need Latex: https://www.latex-project.org/get/

## Running PIVOT
  * Note you MUST launch PIVOT with Rstudio.
  * To run PIVOT, in Rstudio console, use command 
```
library(PIVOT)
pivot()
```

## Troubleshooting
 * URL 'http://xxx.tgz': status was '404 Not Found'
   * Call `chooseCRANmirror()` to select another CRAN mirror.
   
 * Linux specific: Dependency openssl configuration failed
   * Please install the latest libgdal-dev package (apt-get install libgdal-dev)
   
 * Current Known bug:
   * Some times when user press the "launch module" or "clean session" button, new window does not show up. In such cases, please call the last command you see in Rstudio, i.e., `pivot_main()` or `pivot('clean')`
   
 * If you run into other bugs, please report them in github, or email me directly (qinzhu@outlook.com). Thanks!

## Citation

* Qin Zhu, Stephen A Fisher, Hannah Dueck, Sarah Middleton, Mugdha Khaladkar, Young-Ji Na, Junhyong Kim KimLabIDV: Application for Interactive RNA-Seq Data Analysis and Visualization (Preprint) bioRxiv 053348; doi: http://dx.doi.org/10.1101/053348

* For specific analysis, please check the citation listed in the module.



Qin Zhu

Junhyong Kim Lab

University of Pennsylvania

2015 - 2017
