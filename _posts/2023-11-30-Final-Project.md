---
title: Application of Computational Geoscience for Geochemical Characterization of Subduction Zone Volcanic Rocks
description: "A glimpse Results of My Undegraduate Thesis"
date: 2023-11-30 23:21:00 +0700
categories: [Geology, Geochemistry]
tags: [principal component analysis, k-means clustering, gaussian mixture model]     # TAG names should always be lowercase
media_subpath: /assets/img/posts/2023-11-30-Final-Project
authors: [arif]
---

## Pendahuluan
Tugas akhir ini berfokus pada karakterisasi data geokimia di tiga busur kepulauan: Busur Sangihe, Busur Halmahera, dan Busur Filipina Timur. Karakterisasi yang dilakukan menggunakan plot geokimia dan analisis komputasi"

## Metode
1. Diagram Geokimia
   - TAS [(Bas et al., 1986)](https://doi.org/10.1093/petrology/27.3.745)
   - K-Series [(Gill, 1981)](https://doi.org/10.1007/978-3-642-68012-0)
   - Tholeiitic vs. Calc-Alkaline [(Miyashiro, 1974)](https://doi.org/10.2475/ajs.274.4.321) dan [(Irvine and Baragar, 1971)](https://doi.org/10.1139/e71-055.1)
   - Harker [(Harker, 1909)](https://archive.org/details/naturalhistoryof00harkuoft/mode/2up)
   - Spidergram REE [(Sun and McDonough, 1989)](https://doi.org/10.1144/GSL.SP.1989.042.01.19)
   - Spidergram Trace Element [(Pearce, 1983)](https://www.researchgate.net/publication/247434731_Role_of_the_sub-continental_lithosphere_in_magma_genesis_at_active_continental_margin)
2. Analisis Komputasi Geosains
   -  _Principal Component Analysis (PCA)
   -  K-Means Clustering (KMC)
   -  Gaussian Mixing Model (GMM)  

## Data
Data yang digunakan merupakan data yang berasal dari _database_ GeoRoc oleh [Digis Team](https://georoc.mpch-mainz.gwdg.de/georoc/). Pada database didapatkan tiga dokumen, yakni “Luzon Arc”, “Sulawesi Arc”, dan “Halmahera Arc” yang berasal dari kategori “Convergent Margin”. Ketiga dokumen ini berisi total 2987 sampel data geokimia yang terdiri dari batuan vulkanik, beku, sedimen, dan metamorf yang tersebar sepanjang area Sulawesi, Halmahera, Filipina, dan Kalimantan. Ketiga file memiliki informasi asal data, unsur mayor, unsur jejak, dan isotop dari setiap sampel. Dataset ini nantinya akan disaring sehingga dapat diketahui data yang dapat digunakan pada analisis berikutnya.  
Data akan difilter sehingga hanya berisi parameter yang digunakan. proses ini menggunakan python library: pandas. Dataset ini yang kemudian akan digunakan untuk penelitian.

## Output
### Diagram Geokimia 
Gambar di bawah menunjukan karakteristik geokimia menggunakan diagram geokimia

![Diagram TAS](TAS.jpg)
_Diagram TAS (Bas et al., 1986) menunjukan batuan vulkanik yang terbentuk dan terdapat garis pembeda alkali vs. subalkali (Irvine & Baragar, 1971)._

![Diagram K-series](k-series.png)
_Diagram Gill (1981) menunjukan bahwa terdapat dua seri-K pada batuan vulkanik daerah penelitian: medium-K dan high-K._

![Tholeiitic vs. Calc-Alkaline](miyashiro.png)
_Diagram Miyashiro (1979) menunjukan bahwa seluruh batuan vulkanik termasuk pada seri calc-alkaline. Terdapat sebagian kecil anomali yang menunjukan seri tholeiitic._

![Tholeiitic vs. Calc-Alkaline](afm.png)
_Diagram AFM (Irvine & Baragar, 1971) menunjukan bahwa seluruh batuan vulkanik termasuk seri calc-alkaline._

![Harker Mayor Element](harker_mayor.png)
_Diagram Harker (1909) unsur mayor batuan vulkanik daerah penelitian._

![Harker Trace Element](harker_trace.png)
_Diagram Harker (1909) unsur jejak batuan vulkanik daerah penelitian._

![Spidergram](spider.png)
_Diagram spider unsur jejak dan REE daerah penelitian._


### Komputasi Geosains
#### Principal Component Analysis
##### Unsur Mayor

![PCA Unsur Mayor](major_pca.png)
_Biplot dari principal component 1 dan principal component 2 pada unsur mayor daerah penelitian. dihadirkan pula vector loading dari variabel awal._

##### Unsur Jejak

![PCA Unsur Jejak](trace_pca.png)
_Biplot dari principal component 1, principal component 2, dan principal component 3 pada unsur jejak daerah penelitian. dihadirkan pula vector loading dari variabel awal._

#### Analisis Klaster
##### Unsur Mayor

![KMC dan GMM Unsur Mayor](major_kmc_gmm.png)
_Biplot dari analisis k-means clustering (atas) dan gaussian mixture model (bawah)._

##### Unsur Jejak

![KMC Unsur Jejak](trace_kmc.png)
_Biplot k-means clustering pada rasio unsur jejak._

![GMM Unsur Jejak](trace_gmm.png)
_Biplot gaussian mixture model pada rasio unsur jejak._


