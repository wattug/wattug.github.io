---
title: "Assessing Biodiversity in Conservation Area Near Mining Site"
description: "A Study on the Effectiveness of Conservation Efforts Through Remote Sensing and Animal Biodiversity Surveys"
date: 2024-06-24 09:00:00 +0700
mermaid: false
math: true
categories: [ESRI Intern, Natural Resources]
tags: [natural resource, esri, arcgis, time series, geographic information system]     # TAG names should always be lowercase
media_subpath: /assets/img/posts/2024-06-24-Assessing-Biodiversity
authors: [arif]
---
## Introduction
### Purpose
The objective of this project is to build a solution based on GIS technology that can identify the effectiveness of these conservation efforts.

### Premises
Our project is built on the premise that if the conservation efforts by mining companies are effective, we should observe a notable improvement in animal biodiversity within these areas, alongside the expected increase in vegetation.

### Locations
![Locations](lokasi.png){: .w-50}
_Area of Interest._
- Near Gold Mine that located in the southwest of the Batang Toru Ecosystem (BTE), Sumatra Utara. 
- Mining company has designated surrounding conservation areas aimed at protecting and enhancing the local ecosystem.

### Remote Sensing Indices
- Remote sensing indices are crucial tools used in the analysis of satellite imagery to monitor and assess various environmental and ecological conditions.
- The indices selected based on [Parisetal et al (2023) ](https://doi.org/10.3389/ffgc.2023.1020477) and  [Sunkur & Mauremootoo (2024)](https://doi.org/10.52562/injoes.2024.835) research. 

| Indices| Formula |
|--------| --------|
| Normalized Burnt Ratio                               | NBR = (NIR - SWIR) / (NIR + SWIR)   |
| Normalized Difference Vegetation Index               | NDVI = (NIR - Red) / (NIR + Red)    |
| Red-edge Normalized Difference Vegetation Index      | RENDVI = (NIR - Red-edge) / (NIR + Red-edge)   |
| Green Normalized Difference Vegetation Index         | GNDVI = (NIR - Green) / (NIR + Green)    |
| Tasseled Cap Brightness                              | TCB = 0.3037 × Blue + 0.2793 × Green + 0.4743 × Red + 0.5585 × NIR + 0.5082 × SWIR1 + 0.1863 × SWIR2   |
| Tasseled Cap Greenness                               | TCG = −0.2848 × Blue −0.2435 × Green −0.5436 × Red + 0.7243 × NIR + 0.0840 × SWIR1 −0.1800 × SWIR2   |
| Tasseled Cap Wetness                                 | TCW = 0.1509 × Blue + 0.1973 × Green + 0.3279 × Red + 0.3403 × NIR −0.7117 × SWIR1 −0.4572 ×SWIR2   |

### Shannon's Entropy
- It quantifies the uncertainty or randomness in a dataset. In the context of ecology, it is used to measure species diversity within a community. 
- __Calculation:__ The Shannon Index (H) is calculated using the formula \eqref{eq:1}
$$
\begin{equation}
  H = -\sum_{i=1}^{S} p_i \ln(p_i)
  \label{eq:1}
\end{equation}
$$

where $S$ is the total number of species. $P_i$  is the proportion of individuals belonging to the i-th species

### Simpson's Biodiversity Index
- Simpson's Biodiversity Index measures the probability that two individuals randomly selected from a sample will belong to the same species. It is a measure of dominance and is also used to describe species diversity in a community.
- __Calculation:__ The Simpson's Biodiversity Index (D) is calculated using the formula \eqref{eq:2}
$$
\begin{equation}
  D = -\sum_{i=1}^{S} p_i^2
  \label{eq:2}
\end{equation}
$$

where $S$ is the total number of species. $P_i$  is the proportion of individuals belonging to the i-th species

## Data and Method

### Data
This projects has 2 kinds of data: Vegetations and Animals

#### Vegetations
- The vegetations data were derived from Sentinel 2 Imagery from January 2019 until December 2023, 1 dataset per quarter of the year.
- Vegetations data come from __NBR, NDVI,  RENDVI, GNDVI,  TCB, TCG, and TCW__.

#### Animals
- The animal data were created using Survey123 to mimic real field data. The Data will be converted to Simpson's Diversity Index and Shannon's Entropy. 
- The list of animal biodiversity data for this area were obtained from [Key Biodiversity Areas (KBA)](https://www.keybiodiversityareas.org/site/factsheet/23070) Data. This list contain:

1. Panthera Tigris Sumatrae __(Panther)__
2. Macaca sp. __(Primate)__
3. Ichthyophis Paucidentulus __(Amphibia)__
4. Erythropitta Venusta __(Bird)__
5. Tapirus Indicus __(Tapir)__
6. Neolissochilus Thienemanni __(Fish)__

> Please note that the animal location and abundance that presented here is dummy data and used for illustrate the solution's capability only.
{: .prompt-warning }

### Method
![workflow](workflow.png)
_Workflow._
## Results
{% include embed/youtube.html id='K7kdh1xnwLE'%}

## Conclusion
Based on the results, the project successfully developed a GIS-based solution that effectively identifies and evaluates the impact of conservation efforts, also providing valuable insights for future planning and implementation.
