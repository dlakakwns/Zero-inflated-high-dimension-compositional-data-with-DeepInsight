## Zero-inflated High-Dimension Compositional Data with DeepInsight

# Overview

Through the Human Microbiome Project, research on human-associated microbiomes has been conducted in various fields. New sequencing techniques such as Next Generation Sequencing (NGS) and High-Throughput Sequencing (HTS) have enabled the inclusion of a wide range of features of the microbiome. These advancements have also contributed to the development of numerical proxies like Operational Taxonomic Units (OTUs) and Amplicon Sequence Variants (ASVs).

Studies involving such microbiome data often encounter zero-inflated and high-dimensional problems. Based on the need to address these two issues and the recent emphasis on compositional interpretation of microbiome data, we conducted our research.

To solve the zero-inflated problem in compositional microbiome data, we transformed the data onto the surface of the hypersphere using a square root transformation. Then, to solve the high-dimensional problem, we modified DeepInsight, an image-generating method using Convolutional Neural Networks (CNNs), to fit the hypersphere space. Furthermore, to resolve the common issue of distinguishing between true zero values and fake zero values in zero-inflated images, we added a small value to the true zero values.

We validated our approach using pediatric inflammatory bowel disease (IBD) fecal sample data and achieved an area under the curve (AUC) value of 0.847, which is higher than the previous study’s result of 0.83.

For more details on DeepInsight, please visit the official repository: [pyDeepInsight.](https://github.com/alok-ai-lab/pyDeepInsight)

# Data

The raw files can be obtained from NCBI project ID 82109, and the data used in the study is the 'ibd phylo otu' dataset from the R package Corncob.

# Requirements

This project requires the following Python libraries:

+ pyDeepInsight

+ pandas, numpy, scikit-learn

+ torch, torchvision, timm

+ geomstats, IPython, matplotlib, seaborn

+ optuna

Ensure all required dependencies are installed before running the project. This project was developed using Python 3.9, but other versions may also work.

# Files Description

+ Example.ipynb: A Jupyter Notebook providing an example of the overall process, including images.

+ Modified_DeepInsight.ipynb: A notebook supporting the performance claims made in our paper. (Comments are in Korean, apologies for any inconvenience.)

+ Original_DeepInsight.ipynb: A notebook demonstrating the original DeepInsight method’s performance for comparison. (Comments are in Korean, apologies for any inconvenience.)
