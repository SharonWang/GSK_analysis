# GSK_analysis
### Xiaonan Wang
### 26May2020
## Summary: Data analysis of the GSK project

## Introduction 
The analysis was done following the strategy below:

<p align="center"><img src="figures/schematic_view.png" alt="schematic" width="50%"></p>

Two reference datasets were used for data projection:
  1. Cord blood dataset (Unpublished)
  2. [Kuffman dataset](https://github.com/andygxzeng/HSC_Pseudotime/blob/master/scRNA_HSC_denoising.ipynb) (Unpublished)

## Notebooks
This folder contains all jupyter notebooks that were used for the data analysis. To run the notebooks, the Smart-Seq2 preprocessng package would need to be installed first as

    pip install smqpp
  
The main analysis include:
  - <ins>**[CBdata_all](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/CBdata_all.ipynb)**</ins>: Analysis of Cord blood data to generate visualisation layouts as references for projection.
  - <ins>**[Kuffman_all](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/Kuffman_all.ipynb)**</ins>: Analysis of Kuffman data to generate visualisation layouts as references for projection of 0hr data.
  - <ins>**[MPB1234_all](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/MPB1234_all.ipynb)**</ins>: Analysis of all MPB cells together, for better batch correction, data was split by days.
  - <ins>**[MPB_scGen](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/MPB_scGen.ipynb)**</ins>: Batch correction and prediction of perturbation using scGen for MPB 0hr and 62 hr NT and GFP+ cells.
  - <ins>**[MPB1234_Day0](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/MPB1234_Day0.ipynb)**</ins>: Analysis of MPB 0hr cells
  - <ins>**[MPB1234_Day3](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/MPB1234_Day3.ipynb)**</ins>: Analysis of MPB 62hr cells
  - <ins>**[BM789_all](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/BM789_all.ipynb)**</ins>: Analylsis of all BM cells together, for better batch correction, data was split by days
  - <ins>**[BM_scGen](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/BM_scGen.ipynb)**</ins>: Batch correction and prediction of perturbation using scGen for BM 0hr and 62 hr NT and GFP+ cells.
  - <ins>**[BM789_Day0](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/BM789_Day0.ipynb)**</ins>: Analysis of BM 0hr cells
  - <ins>**[BM789_Day3](https://github.com/SharonWang/GSK_analysis/blob/master/Notebooks/BM789_Day3.ipynb)**</ins>: Analysis of BM 62hr cells
  
DPT analysis:
- <ins>**[CB test](https://github.com/SharonWang/GSK_analysis/blob/master/DPT_Notebooks/CBtest.ipynb)**</ins>: Check different data integration and projection methods for CB data Batch 1 and Batch2
- <ins>**[Kuffman test](https://github.com/SharonWang/GSK_analysis/blob/master/DPT_Notebooks/Kuffman_test.ipynb)**</ins>: Check different data integration and projection methods for Kuffman data as reference and MPB Day0 and BM Day0
- <ins>**[DI Method1](https://github.com/SharonWang/GSK_analysis/blob/master/DPT_Notebooks/combat_R.ipynb)**</ins>: Data integration and projection for CB data as reference and MPB and BM data using combat for batch correction (BC) following by destiny R package for calculating diffusion map (DM), corresponding projection (Proj) and diffusion pseudotime (DPT)
- <ins>**[DI Method2](https://github.com/SharonWang/GSK_analysis/blob/master/DPT_Notebooks/combat_scanpy.ipynb)**</ins>: Data integration and projection for CB data as reference and MPB and BM data using combat for CB following by scanpy for calculating DM, corresponding Proj and DPT
- <ins>**[DI Method3](https://github.com/SharonWang/GSK_analysis/blob/master/DPT_Notebooks/fastMNN_scanpy.ipynb)**</ins>: Data integration and projection for CB data as reference and MPB and BM data using scanpy for pca calculation whcih were then corrected by reducedMNN in batchelor R package. The corrected PCA was used in scanpy for calculating DM, corresponding Proj and DPT
- <ins>**[Method comparison](https://github.com/SharonWang/GSK_analysis/blob/master/DPT_Notebooks/Make_comparison.ipynb)**</ins>: Comparing the three methods used for data integration
