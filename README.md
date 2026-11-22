# SWYNEX-Final-Bioinformatics-Report
# Exploratory Analysis and Visualization of Gene Expression Data in Alzheimer's Disease

Internship: SWYNEX Technologies
Project Domain: Bioinformatics and Computational Biology
Dataset: GSE138260 – NCBI Gene Expression Omnibus

# 1. Abstract

Gene expression analysis provides an opportunity to explore molecular patterns associated with diseases using computational approaches. This project involved the exploratory analysis and visualization of a publicly available gene expression dataset, GSE138260, obtained from the National Center for Biotechnology Information's Gene Expression Omnibus (NCBI GEO). The dataset contains human brain samples from individuals with Alzheimer's disease (AD) and healthy controls.
Python-based tools, including Pandas, NumPy and Matplotlib, were used to load the expression matrix, extract sample metadata, organize the samples into groups and examine expression-value distributions. A box plot was generated to compare sample-level mean expression values between the two groups, while a histogram was used to visualize the overall distribution of expression measurements.
The analysis gave me practical experience in handling biological datasets, performing basic descriptive analysis and presenting results through visualizations. The findings are exploratory and do not establish statistically significant gene-expression differences between the groups.

# 2. Introduction

Alzheimer's disease is a progressive neurodegenerative disorder associated with the deterioration of cognitive functions, including memory and learning. Understanding the molecular changes associated with the disease is an important area of biomedical research.

Gene expression data can be used to investigate patterns of gene activity across different biological conditions. Public repositories such as NCBI GEO provide researchers and students with access to experimental datasets that can be explored using computational tools.

This project focuses on the exploratory analysis of a publicly available human brain gene-expression dataset to understand its structure, organize its sample information and visualize expression patterns between Alzheimer's disease and control samples.

# 3. Research Question

How can publicly available gene-expression data from Alzheimer's disease and healthy control brain samples be explored and visualized using Python-based bioinformatics tools?

# Objectives

-Retrieve and examine a publicly available gene-expression dataset from NCBI GEO.
-Understand the structure of the expression matrix and associated sample metadata.
-Organize samples based on their disease status.
-Calculate sample-level mean expression values.
-Visualize expression distributions using appropriate graphical methods.
-Interpret the results while identifying the limitations of descriptive analysis.

# 4. Dataset Description

The dataset selected for this project was GSE138260, retrieved from the NCBI Gene Expression Omnibus.

Parameter                    Description

GEO accession                  GSE138260
Organism                       Homo sapiens
Biological source              Brain tissue
Total samples                  36
Alzheimer's disease samples    17
Control samples                19
Expression matrix dimensions   947,672 rows × 37 columns
The expression matrix contains probe identifiers under the ID_REF column and expression measurements for the 36 samples in the remaining columns.
Sample metadata included disease state, age, gender and tissue information. The samples were classified into Alzheimer's disease and control groups for further exploration.

# 5. Materials and Methods

5.1 Tools and Technologies
The following tools and libraries were used:
-Python: Programming language used for data handling and analysis.
-Google Colab: Cloud-based environment for executing Python code.
-Pandas: Loading, organizing and manipulating tabular data.
-NumPy: Numerical operations and handling expression values.
-Matplotlib: Creating graphical visualizations.
-NCBI GEO: Source of the publicly available gene-expression dataset.

5.2 Dataset Retrieval and Loading
The GSE138260 Series Matrix file was downloaded from NCBI GEO in compressed .txt.gz format.
The dataset was loaded into Python using Pandas. The gzip module was used to handle the compressed file, and the expression matrix was separated from the GEO metadata section.

5.3 Metadata Extraction
Sample information was extracted from the Series Matrix file. The metadata included:
-GEO sample accession identifiers
-Sample titles
-Disease state
-Age
-Gender
-Tissue
The samples were categorized into two groups: Alzheimer's disease (AD) and Control.
The resulting metadata table contained 36 samples.

5.4 Sample-Level Mean Expression Calculation
The mean expression value was calculated for each sample by taking the average across all available probe measurements.
These values were combined with the corresponding sample metadata to enable descriptive comparisons between the AD and control groups.

5.5 Data Visualization

Two visualizations were generated:

A. Box Plot – Comparison of AD and Control Samples
A box plot was generated to compare the distribution of sample-level mean expression values between Alzheimer's disease and control samples.
This visualization helps examine the median, spread and variability of the sample-level averages.

B. Histogram – Distribution of Gene Expression Values
A histogram was generated using a reproducible random sample of 10,000 probe rows from the expression matrix.
The expression values from the selected probes across all 36 samples were used to examine the overall distribution of expression measurements.

# 6. Results and Observations

6.1 Dataset Organization
The dataset contained 36 human brain samples, consisting of:
17 Alzheimer's disease samples.
19 healthy control samples.
The metadata extraction process enabled the classification of samples according to their disease state, providing the basis for subsequent comparisons.

6.2 Box Plot Analysis

The box plot provided a visual comparison of sample-level mean expression values between the AD and control groups.
The calculated group averages were approximately:
AD: 5.1896
Control: 5.1878
The two averages were relatively close, indicating that the overall sample-level mean expression values were similar in this descriptive comparison.
However, this does not establish that individual genes have similar expression levels between the groups. Changes in specific genes may not be reflected by an overall sample average.

6.3 Histogram Analysis

The histogram illustrated the distribution of expression measurements across the randomly selected probe rows.
The visualization showed that expression measurements were concentrated across a range of values, with a tail extending towards higher expression values.
This helped demonstrate how large-scale gene-expression measurements can be explored visually to understand their overall distribution.

6.4 Overall Findings

The project demonstrated how a publicly available biological dataset can be retrieved, organized and explored using Python.
The combination of metadata extraction, sample-level calculations and graphical visualization provided an introductory understanding of computational analysis of gene-expression data.

# 7. Discussion

The analysis provided practical experience in working with a large biological expression matrix and its associated metadata.

The box plot offered a descriptive comparison of the average expression values of the two sample groups, while the histogram provided an overview of the distribution of expression measurements.

An important observation from this project is that overall sample-level averages alone cannot explain the molecular differences associated with a complex disease such as Alzheimer's disease.

A more detailed investigation would require probe-to-gene annotation, differential expression analysis, appropriate statistical testing and biological interpretation of the identified genes.

Therefore, the current analysis should be considered an exploratory step towards more advanced gene-expression studies.

8. Limitations

The project had the following limitations:

-The analysis was restricted to descriptive statistics and visualization.
-Sample-level mean expression values were calculated across all probes, which may conceal gene-specific expression differences.
-No differential gene-expression analysis or statistical significance testing was performed.
-Individual probe identifiers were not systematically mapped to their corresponding genes.
-The histogram was generated from a random subset of 10,000 probe rows rather than the complete expression matrix.
-The analysis did not include additional functional enrichment or pathway analysis.
-These limitations should be considered when interpreting the observations.

# 9. Conclusion

This project demonstrated the application of Python-based computational tools for the exploratory analysis of gene-expression data obtained from NCBI GEO.

Using the GSE138260 dataset, sample metadata were extracted, samples were classified into Alzheimer's disease and control groups, and sample-level mean expression values were calculated. Box plot and histogram visualizations were used to examine the distribution of expression measurements.

The project strengthened practical understanding of biological data handling, descriptive analysis and visualization using Python. It also highlighted the importance of selecting appropriate analytical methods and recognizing the limitations of preliminary computational results.

Further work involving differential gene-expression analysis, gene annotation and functional enrichment could provide deeper insights into the molecular mechanisms associated with Alzheimer's disease.

# 10. References

National Center for Biotechnology Information (NCBI). Gene Expression Omnibus (GEO): GSE138260. Available at: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE138260

McKinney, W. (2010). Data Structures for Statistical Computing in Python. Proceedings of the 9th Python in Science Conference, 56–61.

Harris, C. R., et al. (2020). Array programming with NumPy. Nature, 585, 357–362.

Hunter, J. D. (2007). Matplotlib: A 2D Graphics Environment. Computing in Science & Engineering, 9(3), 90–95.
