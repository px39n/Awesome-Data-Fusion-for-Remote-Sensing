# Awesome Data Fusion [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)
List of reference,algorithms, applications in RS data fusions (**contribution are welcome**)
<img src="https://www.mdpi.com/remotesensing/remotesensing-10-00527/article_deploy/html/images/remotesensing-10-00527-g001.png" alt="drawing" width="600"/>
## Table of Contents


  * [Overview of Data Fusion](#overview-of-data-fusion)
    + [Trends and Literature Reviews](#trends-and-literature-reviews)
    + [Basic Concept](#basic-concept)
    + [Sensors](#sensors)
  * [Focus, Challengings, Algorithms/Models, Quality Assessment](#focus--challengings--algorithms-models--quality-assessment)
    + [Branch of Research Focus(Taxonomy)](#branch-of-research-focus-taxonomy-)
    + [Current Challengings](#current-challengings)
    + [Algorithms](#algorithms)
      - [1.Single Dimension Traditional Algorithms (Pan-Sharpening, Spectral-matching)](#1single-dimension-traditional-algorithms--pan-sharpening--spectral-matching-)
      - [2. Spatiotemporal Dimension Traditional Methods（Reconstruction)](#2-spatiotemporal-dimension-traditional-methods-reconstruction-)
      - [3.Deep Learning in Fusion (Task driven)](#3deep-learning-in-fusion--task-driven-)
    + [Quality Assessment](#quality-assessment)
  * [Community](#community)
    + [IEEE GRSS data fusion contest](#community)
    + [Software and Open Source Tool](#software-and-open-source-tool)
      - [Cloud Services](#cloud-services)
      - [Useful Library](#useful-library)
    + [Database](#database)
  * [TERMS](#terms)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## Overview of Data Fusion

### Trends and Literature Reviews
*There are popular topics and review literatures in different period.*

**1992~2000**: Data fusion, spatial resolution
- Data Fusion Subpanel of the Joint Directors of Laboratories (JDL. 1991)
- Fusion of satellite images of different spatial resolutions([Linas et al.1997](29610623_Fusion_of_satellite_images_of_different_spatial_resolutions_Assessing_the_quality_of_resulting_images))

- Multisensor Image Fusion in Remote Sensing: Concepts, Methods and Applications([Pohl et al.1997](https://www.researchgate.net/publication/200459274_Multisensor_Image_Fusion_in_Remote_Sensing_Concepts_Methods_and_Applications))
- Some terms of reference in data fusion([Wald,1999](https://www.researchgate.net/publication/3202105_Some_terms_of_reference_in_data_fusion))

**2001~2010**: classification, unsupervision, change detection, model, multi-resolution, quality, feature extraction  Wavelet transform

- #Handbook of Multisensor Data Fusion([Hall et al.2001](https://books.google.com/books?hl=en&lr=&id=6Im9BwAAQBAJ&oi=fnd&pg=PP1&dq=data%20fusion&ots=lAMV_hUBnr&sig=XFiQ5zbwqxqdTAivA0OmBMwxf3Q))
- Mathematical Techniques in Multisensor Data Fusion ([Hall et al. 2004](https://books.google.co.uk/books?hl=en&lr=&id=HxjDMcJWLYwC&oi=fnd&pg=PR13&dq=data%20fusion&ots=kecv10tcqu&sig=WvhHHipHmBoDdLnktJLkegKEeJQ&redir_esc=y#v=onepage&q=data%20fusion&f=false))
- Multi-Sensor Data Fusion: An Introduction ([Mitchell 2007](Multi-Sensor%20Data%20Fusion:%20An%20Introduction))
- Synthesis of Multispectral Images to High Spatial Resolution: A Critical Review of Fusion Methods Based on Remote Sensing Physics([Thomas et al.2008](https://ieeexplore.ieee.org/abstract/document/4447659))
- Decision Fusion for the Classification of Hyperspectral Data: Outcome of the 2008 GRS-S Data Fusion Contest ([Licciardi et al.2009](https://ieeexplore.ieee.org/abstract/document/5286249))
- Advances in Multi-Sensor Data Fusion: Algorithms and Applications ([Dong et al.2009](https://www.mdpi.com/1424-8220/9/10/7771))
- Multi-source remote sensing data fusion: status and trends [(Zhang et al.2010](https://www.tandfonline.com/doi/full/10.1080/19479830903561035))

**2011~2021**:hyperspectum, deep learning, Heterogeneous, fusion framework, sparse expressions.
- A review of remote sensing image fusion methods([Ghassemian et al.2016](https://www.sciencedirect.com/science/article/abs/pii/S1566253516300173?via%3Dihub)
- Data Fusion and Remote Sensing: An ever-growing relationship([Schmitt et al.2016](https://ieeexplore.ieee.org/abstract/document/7740215/))
- Spatiotemporal Fusion of Multisource Remote Sensing Data: Literature Survey, Taxonomy, Principles, Applications, and Future Directions([Zhu et al.2018](https://www.mdpi.com/2072-4292/10/4/527/htm))
- Spatiotemporal Image Fusion in Remote Sensing ([Belgiu et al.2019](https://www.mdpi.com/2072-4292/11/7/818))
- Deep Learning in Remote Sensing: A Comprehensive Review and List of Resources([Zhu et al.2019](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8113128/references#references))

### Basic Concept
**DOD:** Data fusion is a multilevel, multifaceted process dealing with the automatic detection, association, correlation, estimation, and combination of data and information from multiple source.
**Community:** Data fusion is a formal framework in which are expressed means and tools for the alliance of data originating from different sources. It aims at obtaining information of greater quality; the exact definition of ‘greater quality’ will depend upon the application


### Sensors

| Satellite | Sensor | Spatial Resolution | Band | Revisit Cycle |  
|--|--|--|--|--|
| NOAA | AVHRR | 1.1km |VIS,NIR,TIR |12h |
| Terra/Aqua| MODIS| 250m,500m,1000m|36bands| 1d |
| Terra| ASTER| 15m,30m,90m| 14bands(VIS-TIR) | 16d| 
| Lansat| MSS| 79m| VNIR | 18d| 
| Terra| MSS+TM| 30m,120m| VNIR,TIR | 16d| 
| Terra| ETM+| 30m,60m|VNIR,TIR | 16d| 
| Terra| OLI| 30m,100m|VNIR,TIR | 16d | 
| OrbView-2| Sealifts| 1km|VIR,NIR,pan| 1d | 
| SPOT| HRV| 20m| 3VNIR | 26d | 
| SPOT| VGT| 1.15km| 3VNIR+SWIR | 26d | 
| SPOT| HRG/HRS/VGT| 10m| | 26d | 
| ENVISAT | MERIS |300m | 15(390-1040nm | 35d|  
| Sentinel-2 | MSI | 10m,20m,60m | VNIR, SWIR |5days |  
| Sentinel-1 | SAR |>5m| C band | 12 
|Sentinel-3|SLSTR,OLCI,SRAL,DORIS |~300M | optical, micro,  | 1d 
| HJ-1A/1B | UPDATING | 30m| | 31d
| TH-1 |UPDATING| 10m | | 58d
| BJ-1 |UPDATING|32m | | 
| CBERS-01/02 |UPDATING|20m-150m | | 26d
| ZY-1 02B |UPDATING|20m | | 26d
| ZY-2 02C |UPDATING|10m | | 55d
| SJ-9A | UPDATING |10m | | 69d
| IRS-P3 | WIFS/MOS |188m | | 5d
| updating  |  | | | 

## Focus, Challengings, Algorithms/Models, Quality Assessment
### Branch of Research Focus(Taxonomy)
*Depending on the main problem solved by the model/algorithm,  the development of data fusion can be divided into many areas*

**According to process levels:** Pixel, Attribute, Decision
**According to Principle:** Weighted function based, Decomposition  based, Learning based (including sparse dictionary,DL), Bayesian based, Hybrid based 
**According to number of Sensors:** From 1 to N
**According to sensors:** Homogeneous fusion, Heterogeneous fusion (NIR,-VIS, Optical-SAR, Optical-Thermal, hyper-Multi etc.,), Remote sensing site fusion, Remote sensing non-observation fusion (Data assimilation)
**According to mechanisms:** Competitive integration, Complementary integration(like temporal and spatial), Cooperative integration(like 3D reconstruction)
**According to Dimension**: Spatial Dimension Enhancement, Spectral Dimension Enhancement, Time dimension enhancement, End to End.
**According to Applications**: Pan sharpening, Spatiotemporal, Change detection, Object recognition, Agriculture, Ecology etc.,
**According to procedure:** Matching, Co-registration, Process, Quality Assessment.

### Current Challengings
*In almost every small direction (as shown in the previous subsection). There are a number of issues so authors only list some most important challenges to demostrate.*

**Topological Issues:**
Geometric Correction, Error caused by height of buildings/or DEM. BRDF adjustment

Figure1. Error due to deviation in DEM

![enter image description here](https://github.com/px39n/Awesome-Data-Fusion-for-Remote-Sensing/blob/main/imgs/elevation.png?raw=true)

Figure2. Relationship between error and Angle

![enter image description here](https://github.com/px39n/Awesome-Data-Fusion-for-Remote-Sensing/blob/main/imgs/relationship.png?raw=true)
**Radiometric Issues:** 
Radiometric Correction, Band pass adjustment
**Process Issues:**
- **General level:** Computation Speed(Cloud service), abrupt change (in land use), Multimodal sensor. heterogeneous region
- **For traditional methods:** Un-Mixing(Big error, Spatial variability within coarse pixels), sparse representation (Insufficient a priori knowledge), landcover(Landscape heterogeneity, Abrupt change)
- **For Deep Learning:**  Change Detection(Seasonal change, vegetation, Transferable),  computation, feature-level alignment, transferable, physics prior knowledge. 



### Algorithms
There are currently more than 200 spatio-temporal models, so only part of baseline models or polular papers are included.

#### 1.Single Dimension Traditional Algorithms (Pan-Sharpening, Spectral-matching)
(Pan-sharpening by using a pair of images registered)
| Purpose| Principle | Method | Paper |  Code| Features
|--|--|--|--|--|--|
| Spatial | Component (+) | Principle Component Analysis(PCA) |Shettigara et al.1992 | Updating
| Spatial |  +| Intensy-Hue-Saturation(IHS) | Tu et al.2001|Updating
| Spatial | + | Brovey Transform(BT) | Tu et al.2005|Updating
| Spatial | + | Gram-Smidt(GS) | Aiazzi et al.2007|Updating
| Spatial | +  | GS adaptive(GSA) | Aiazzi et al.2007|Updating
| Spatial |  + | GIHS adaptive(GIHSA) | Aiazzi et al.2007|Updating
| Spatial | Unmaxing  | MMT |[(Zhukov et al.1999)](https://ieeexplore.ieee.org/abstract/document/763276) | Updating
| Spatial |  + | MMT(MERIS,Lansat)|[(Milla et al.2008)](https://ieeexplore.ieee.org/abstract/document/4512324) | Code  | constraints, Positive of End Member
| Spatial | + | LAC-GAC NDVI |([MAselli, 2011](https://www.tandfonline.com/doi/abs/10.1080/01431160110104755?casa_token=OGtmv7j1CRcAAAAA:Whs-bZ-yGG54IqS1L94ThnIMksiogU9CGaRe69ysWSCzF8HysHQZ0JpEzQACcC5zqtS6L103pkB0)) | Code
| Spatial | Baysian | BME | ([Li et al.2013](https://www.sciencedirect.com/science/article/pii/S0034425713001004)) | [Code](https://github.com/PythonCharmers/maxentropy)
| Spatial | Hybrid|Updating| |
| Spectral| Linear | Wavelet Transform|Nunez et al.1999 |Updating
| Spectral| + |High-pass filtering | Chavez et al.1991|Updating
| Spectral| + | Curvelet Transform | Nencini et al.2007 |Updating
| Spectral| + | Contour Transform | do and Vetterli 2005 |Updating
| Spectral| + |Laplacian Pyramid |Schmitt and Zhu, 2005 |Updating
| Spectral|+  |Smoothing Filter-based intensity modulation |Liu,2000 |Updating
| Spectral| Unmixing | Spectral Unmixing | Bendoumi et al.2014 |
| Spectral| + | Nonnegative Matrix Unmixing | Huang et al.2008|Updating
| Spectral| + | Coupled Nonnegative Matrix Unmaxing| Yokoya et al.2012|Updating
| Spectral| Bayesian | Maximum a posteriori|Hardie et al.2004 |Updating
| Spectral| Learning | Sparse Representation | |
| Spectral|+| Analysis Sparse Model | |
| Spectral|+| MRA DNN |[Azarang et al.2017](https://ieeexplore.ieee.org/abstract/document/7983017/) | Code
| Spectral| + | PNN | [Li et al.2012](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.482.8719)|Updating
| Spectral|+| DRPNN |[Wei et al.2017](https://ieeexplore.ieee.org/document/8012503) [Matlab](https://github.com/Decri/DRPNN-Deep-Residual-Pan-sharpening-Neural-Network)|Residual Network
| Spectral| + | MSDCNN | [Zhou et al.2019](https://ieeexplore.ieee.org/abstract/document/8709694) | [Python](https://github.com/Decri/Multi-Scale-and-Depth-CNN-for-Pan-sharpening)
| Spectral| Hybrid|| |


#### 2. Spatiotemporal Dimension Traditional Methods（Reconstruction)
(Normally Prediction by fusing two high temporal and high spatial resolution sensors with correction)
|Sensor| Principle | Method | Paper | Code| Features
|--|--|--|--|--|--|
| Landsat&MODIS| Weighted Function |STARFM|（[Gao et al.2006](https://ieeexplore.ieee.org/abstract/document/1661809)) |[Python](https://github.com/topics/starfm)
|+ |+  |STAARCH| ([Hilker et al.2009](https://www.sciencedirect.com/science/article/pii/S003442570900087X)) | Code | Cloud and Snow Cover
| +|+  |ESTARFM|([Zhu et al.2010](https://www.sciencedirect.com/science/article/pii/S0034425710001884)) | [IDL,Python](https://xiaolinzhu.weebly.com/open-source-code.html) |Enhancement in Heterogeneous region 
| MODIS&landsat| + |RWSTFM|([wang et al.2017](https://www.mdpi.com/2072-4292/9/10/990)) |Code | kriging Based
| MODIS&landsat|+ |SADFAT|[Weng et al.2014](https://www.sciencedirect.com/science/article/pii/S0034425714000479) |Code | Consider Annual temperature Cycle
| Unlimited |+  |STITFM|[Wu et al.2014](https://www.sciencedirect.com/science/article/pii/S0034425714003563) |Code | Multi-Sensor LST
| |  +|STVIFM|[Liao et al.2017](https://www.mdpi.com/2072-4292/9/11/1125)|Code | growth stages
| |Unmixing |ESTDFM|([Zhang et al.2013](https://www.mdpi.com/2072-4292/5/10/5346)) | 
| | + |MSTDFA| [Wu et al.2015](https://www.mdpi.com/1424-8220/15/9/24002/htm)|Code | sensor adjustment by linear model
| | + |OB-STVIUM| ([Lu et al.2016](https://www.sciencedirect.com/science/article/pii/S0034425716302851)) |Code | Consideration of Phenology Change
| Temporal| Bayesian |NDVI-BSFM| |
| | Learning |SPSTFM| ([Huang et al.2012](https://ieeexplore.ieee.org/abstract/document/6169983)) | Code| sparse representation 
| | +|One-pair image learning method| ([Song et al.2012](https://ieeexplore.ieee.org/abstract/document/6329421)) | Code| sparse representation 
| Landsat&AHVRR|+  |EBSCDL|[Wu et al.2015](https://ieeexplore.ieee.org/abstract/document/7160722) |
 | Landsat&MODIS| + |ELM| ([Liu et al.2016](https://ieeexplore.ieee.org/abstract/document/7748638) ) | Code| [Matlab](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7748638/figures#figures)
 | Landsat&MODIS| + |CSSF| ([Wei et al.2017](https://ieeexplore.ieee.org/abstract/document/8036397)) | Code| Compression downsampling
 | Landsat&MODIS| + |WAIFA| [Moosavi et al.2015](https://www.sciencedirect.com/science/article/pii/S0034425715301036)| | wavelet&ANN
  | Landsat&MODIS| + |STFDCNN| [Song et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8291042)| Code| Transition Image
 | | + |DCSFTN| | Code|
 | | Hybrid|FSDAF| ([Zhu et al.2016](https://www.sciencedirect.com/science/article/pii/S0034425715302042))| Abrupt Change 
 | |+ |NDVI-LMGM| ([yu et al.2015](https://www.mdpi.com/2072-4292/7/6/`7865`/htm))| linear growth&unmixing
 |Two Time series| Others |STAIR| ([Luo et al.2015](https://www.sciencedirect.com/science/article/pii/S0034425718301998))| Difference, Cloud
 |Multi Time series| Others |STAIR2| ([Luo et al.2020](https://www.mdpi.com/2072-4292/12/19/3209/htm))| 

#### 3.Deep Learning in Fusion (Task driven) 
Deep learning normally focus on a specific task. And nomally in format of End-to-End way.
|Task| Source | Method | Paper | Code| Features
|--|--|--|--|--|--|
| Pan-Sharpening| Low&High |CNN|[jin et al.2016](https://link.springer.com/article/10.1007/s11220-016-0135-6)|Code | Resolution enhancedment of MSS
| Pan-Sharpening| Low&High |CNN|[G Masi et al.2016](https://scholar.google.com/scholar?as_q=Pansharpening+by+convolutional+neural+networks&as_occt=title&hl=en&as_sdt=0%2C31)|Code | End-to-End
| Super Resolution| Low&High |CNN|[Yuan et al.2016](https://scholar.google.com/scholar?as_q=Pansharpening+by+convolutional+neural+networks&as_occt=title&hl=en&as_sdt=0%2C31)|[Code](https://github.com/junjun-jiang/Hyperspectral-Image-Super-Resolution-Benchmark) | End-to-End,Transfer Model from CV, hyperspectrum
| Super Resolution| Low&High |Deep Residual Convolutional Neural Network|[Wang et al 2017](http://www.ict.griffith.edu.au/~junzhou/papers/C_ICIG_2017.pdf)|[Code](https://github.com/junjun-jiang/Hyperspectral-Image-Super-Resolution-Benchmark) | End-to-End,Transfer Model from CV, hyperspectrum
| Super Resolution| Low&High |SSF-CNN|[X. Han et al 2018](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8451142)|[Code](https://github.com/junjun-jiang/Hyperspectral-Image-Super-Resolution-Benchmark) | End-to-End,Transfer Model from CV, hyperspectrum
| Super Resolution| Low&High |Deep Neural Network|[R. Dian et al.2017](https://drive.google.com/open?id=1FIyVL9c8jlDY3heEZ57nGvpSDZc0mkeT)|[Code](https://github.com/renweidian/DHSIS) | 
| Super Resolution| Low&High |Sparse Dirichlet-Net|[Y. Qu et al.2018](https://arxiv.org/abs/1804.05042)|[Code](https://github.com/aicip/uSDN) | 
| Super Resolution| Low&High |Deep Neural Network|[Y. Qu et al.2018](https://arxiv.org/abs/1902.00301)|[Code](https://github.com/acecreamu/deep-hs-prior) | 
| Super Resolution| Low&High |Deep Neural Network|[Y. Qu et al.2020](https://www.mdpi.com/2072-4292/13/2/167/htm)|[Code](https://github.com/acecreamu/deep-hs-prior) | Chen
Registration and SR| Low&High |Deep Neural Network|[Y. Qu et al.2018](https://ieeexplore.ieee.org/document/8897135)|[Code](https://github.com/zhouyuanzxcv/Hyperspectral) | 
Registration| SAR&Optical |Deep Neural Network|[Mou 2017 et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7924548) | Patch-based
| Classification| Multi |CNN|[Lagrange et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7326745)|[Code](https://github.com/acecreamu/deep-hs-prior) | Comparision of existing
| Classification| Multi |FusioNet|[Hu et al.2017](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7924565)|[Code](https://github.com/acecreamu/deep-hs-prior) | Feature Level, two Stream
| Classification| Multi |DeepNetsForEO|[Audebert et al.2017](https://link.springer.com/chapter/10.1007/978-3-319-54181-5_12ithub # Semantic Segmentation of Earth Observation Data Using Multimodal and)|[Code](https://github.com/nshaud/DeepNetsForEO/blob/master/legacy/README.md) | Feature Level, two Stream
| Classification| VNIR-DSM |DeepUNet|[Audebert et al.2017](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8486170)|[Code](https://github.com/nshaud/DeepNetsForEO/blob/master/legacy/README.md) | Channel Packing
| Recognition| Hyper&SAR |Dual DCNN|[Lagrange et al.2018](https://arxiv.org/abs/1605.05462)|[Code](https://github.com/seongjunyun/CNN-with-Dual-Local-and-Global-Attention) | Feature Level, two Stream
| Recognition| Multi&SAR |Multi-TaskUNet|[JIAN et al.2019](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8554076)|[Code](https://github.com/seongjunyun/CNN-with-Dual-Local-and-Global-Attention) | Multi-Task(Edge, Biniary),xception
| Registration| Optical&SAR |Siamese|[Mou et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7924548)|[Code](https://github.com/seongjunyun/CNN-with-Dual-Local-and-Global-Attention) | Feature Level, two Stream, semi-auto- Label
| Registration| Optical&SAR |3 DNN|[Hughes et al.2020](https://www.sciencedirect.com/science/article/pii/S0924271620302598?via%3Dihub)|[Code]() | hot map, goodness
| Registration| Optical&SAR |Siamese|[He et al.2018](https://www.mdpi.com/2072-4292/10/2/355)|[Code]() |
| Registration| Optical&SAR |Pseudo-Siamese CNN|[Hughes et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8314449)|[Code]() |  
| SAR 2 Optical| SAR |GANs|[Reyes et al.2018](https://www.mdpi.com/2072-4292/11/17/2067/htm)|[Code](https://github.com/seongjunyun/CNN-with-Dual-Local-and-Global-Attention) | Feature Level, two Stream, semi-auto- Label
| SAR 2 Optical(Cloud removal)| SAR |DRN|[Meraner et al.2018](https://pubmed.ncbi.nlm.nih.gov/32747852/)|[Code](https://github.com/ameraner/dsen2-cr) | cloud removal
| SAR 2 Optical| SAR |sar2opt|[Toriya et al.2019](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8898605?denied=)|[Code]() |
| Growth Prediction| Multi |CNN|[Scarpa et al.2018](https://www.mdpi.com/2072-4292/10/2/236/htm)|[Code](https://github.com/antoniomazza88/SAR2NDVI_CNN) | pixel level, Sentinel,NDVI fusion and pixel fusion
| Growth Prediction| SAR&VNIR |Random Forest|[hECKEL et al.2020](https://www.mdpi.com/2072-4292/12/2/302/htm)|[Code]() | pixel level, Sentinel



### Quality Assessment
**1.Assessment Index With Reference Images.**
| Index | Description | Dimension  |  Reference 
|--|--|--|--|
|Spectral angle|updating | spectral| Updating
General image quality index|updating|spectral| Updating
|Root Mean Square Error|updating|spectral&temporal| Updating
|Relative mean spectral error| updating|spectral&temporal
|Signal-to-noise ratio| updating|spatial| Updating
|Peak signal-to-noise ratio|updating |spatial| Updating
|Correlation coefficient|updating |spatial&temporal| Updating
|Structural similarity coefficient| |spatial&temporal| Updating
|Global integrated error index| updating|spatial&spectral| Updating
|Average error|updating |spatial| Updating
**2.Assessment Index Without Reference Images.**
| Index | Description | Dimension  |  Reference 
|--|--|--|--|
|Average value | updating|spatial,spectral
|Variance | updating|spatial,temporal| Updating
|Standard deviation |updating |spatial,temporal| Updating
|Information entropy | updating|spatial,temporal| Updating
|Mean gradient |updating|spatial,temporal| Updating

## Community

### IEEE GRSS data fusion contest([Link](http://www.grss-ieee.org/grss-webinars/))
**Year: 2020** 
**Title**:  Global Land Cover Mapping with Weak Supervision
**Data**: MSS, SENTINEL MSS

Track1:
Main Author | Approach| Code |
|--|--|--|
Robinson| A combination of iterative clustering and epitome representations | [Code](https://github.com/microsoft/landcover) |
Yu Xia| Multi-branch fusion of unsupervised multi-resolution segmentation, random forest classification of remote sensing indexes, and convolutional neural network predictions with post-processing based on expert priors | [WHU_YuXia](https://github.com/microsoft/landcover) |
Daniele Cerra| Automated label pre-processing, a Gaussian Naive Bayes classifier trained on cluster centroids, and classes obtained by k-means clustering and random forests with bag of words features, followed by classification refinement designed for specific classes | [Pineapples](https://github.com/microsoft/landcover) |
Track 2:
Main Author | Approach| Code |
|--|--|--|
Huijun Chen| An ensemble of random forests trained on refined labels | [Antonia](https://github.com/microsoft/landcover) |
Daniele Cerra| As Track 1 third, but random forests trained on high-resolution labels for validation data | [Pineapples](https://github.com/microsoft/landcover) |
Shuting Yin| A combination of random forests, k-means, and DeepLabv3++ with postprocessing and retraining | [dfchen](https://github.com/microsoft/landcover) |


**Year: 2019** 
**Title**:  Reconstruct both a 3D geometric model and a segmentation of semantic classes for an urban scene
**Data**: WorldView-3, VIR, NIR, LiDAR

Track 1: Single-view semantic 3D

Main Author | Approach| Code |
|--|--|--|
Saket Kunwar| An ensemble of random forests trained on refined labels | [nest](https://github.com/microsoft/landcover) |
Zhuo Zheng| A pyramid on pyramid network based on an encoder-dual decoder framework | [RSIDEA-WHU](https://github.com/microsoft/landcover) |
Track 2: Pairwise semantic stereo
Main Author | Approach| Code |
|--|--|--|
Hongyu Chen| A modified version of Pyramid Stereo Matching Network (PSMNet) and Disparity Fusion Segmentation Net (DFSN) | [BurningAllthing](https://github.com/microsoft/landcover) |
Rongjun Qin| U-Net and Pyramid Stereo Matching Network (PSMNet) | [qin.324](https://github.com/microsoft/landcover) |

Track 3: Multi-view semantic stereo
Main Author | Approach| Code |
|--|--|--|
Pablo d’Angelo| Semi-global matching and an ensemble of CNN classifiers with ad hoc detectors | [Panoptes](https://github.com/microsoft/landcover) |
Rongjun Qin| Semi-global matching and U-Net | [qin.324](https://github.com/microsoft/landcover) |
Track 4: 3D point cloud classification
Main Author | Approach| Code |
|--|--|--|
Lian Yanchao| An ensemble of random forests trained on refined labels | [nest](https://github.com/microsoft/landcover) |
Jia Meixia| Attention-SIFT Net (AS net) based on Pointnet++ and PointSIFT | [aijinli0613](https://github.com/microsoft/landcover) |

**Year: 2018** 
**Title**:  urban land use and land cover classification
**Data**: Hyper, Multi, Lidar, RGB(5cm)
updating
Main Author | Approach| Code |
|--|--|--|
Yonghao Xu| Fully convolutional networks and post-classification with topological relationships among different objects | [Gaussian](https://github.com/microsoft/landcover) |
Daniele Cerra| Deep convolutional and shallow neural networks on a simplified set of classes, completed by a series of specific detectors and ad hoc classifiers | [dlrpba](https://github.com/microsoft/landcover) |
Sergey Sukhanov| Ensemble learning based on several classifiers, including convolutional neural networks, gradient boosting machines, and random forests, followed by post-processing techniques | [AGTDA](https://github.com/microsoft/landcover) |

2017,2016,2015 are updating!

### Software and Open Source Tool
*We will focus on cloud computing and some important machine learning libraries*
#### Cloud Services
- Google Earth Engine
- AWS
- Updating
#### Useful Library 
- Updating

### Database

-   [CAVE dataset](http://www.cs.columbia.edu/CAVE/databases/multispectral/)
-   [Harvard dataset](http://vision.seas.harvard.edu/hyperspec/explore.html)
-   [iCVL dataset](http://icvl.cs.bgu.ac.il/hyperspectral/)
-   [NUS datase](https://sites.google.com/site/hyperspectralcolorimaging/dataset/general-scenes)
-   [NTIRE18 dataset](http://www.vision.ee.ethz.ch/ntire18/)
-   [Chikusei dataset](https://www.sal.t.u-tokyo.ac.jp/hyperdata/)
-   [Indian Pines, Salinas, KSC et al.](http://www.ehu.eus/ccwintco/index.php/Hyperspectral_Remote_Sensing_Scenes)
- [Sen1-2 Dataset](https://arxiv.org/abs/1807.01569)
- [SEN12MS](https://arxiv.org/abs/1906.07789)
##  TERMS 
 *There are terms which are slightly different from those in other areas.*

**Measurements（SIGNAL/image）**: Primarily the outputs of a sensor，represent the raw information, normally in format of singal, images. The elementary support of the measurement is a **pixel** in the case of an image, and is called a sample in the general case

**Object**: It is defined by its properties, e.g., its color, its materials, its shapes, its neighborhood, etc. It can be a field, a building, the edge of a road, a cloud, an oceanic eddy, etc.

**attribute(Feature)**: It is a property of an object.
**Mathematical attribute**: aggregation of measurements made for each of the elements of the object
**Modality**: It refers to the raw input used by the sensors.

**Spatial context** of a pixel, computed by local variance, or structure function or any spatial operator. This operation can be extended to time context in the case of time-series of measurements. Equivalent terms are local variability, local fluctuations, spatial or time texture, or pattern.


