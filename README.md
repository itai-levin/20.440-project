# Identifying biomarkers for traumatic brain injury (TBI)-induced dementia using PLSDA on patient RNA-seq data

## Overview
The repository contains the data and code to produce a visualization of a subset of the 
Fragments per Kilobase Millions (FPKM) data from the Allen Brain Institute's Aging, 
Dementia, and TBI study (https://aging.brain-map.org/rnaseq/search).
The purpose of the data visualization is to ensure that we are able to open and
manipulate the data to a state that shows differential gene expression for different 
brain samples.

## Data
The data is publicly available and was downloaded from 
https://aging.brain-map.org/download/index
This visualization and subsequent analysis will use the normalized FPKM values in a csv
file. These data were directly obtained from the Allen Brain Institute (ABI). 
To generate these data, the team from the ABI did the following:
RNA sequencing was performed on dissected sections from 107 brains.
Raw reads were aligned to the human genome, which generated the FPKM data
Normalization steps were performed to reduce batch effects and account for RNA
quality differences between samples.
For our visualization, we further normalized the data by z-scoring, i.e. subtracting the 
mean FPKM value by gene and dividing by the standard deviation of the FPKM values
for that gene. We also removed genes and samples which had no reads mapped to
them.

## Folder Structure
The code to produce the visualization is in a Jupyter Notebook:
20-440_project_2pager.ipynb
The data is in the csv file:
fpkm_table_normalized.csv

## Installation
The visualization requires Python 3.x
The required packages for this visualization are listed in requirements.txt and can be 
installed by running: 
`pip -r intstall requirements.txt`

To run the code to produce the visualization, open the code in Jupyter Notebook
and proceed through the cells. The figure will be saved as `datavisualization.png`

