
# Awesome Data Fusion [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)
List of reference,algorithms, applications in RS data fusions (**contribution are welcome**)
<img src="https://www.mdpi.com/remotesensing/remotesensing-10-00527/article_deploy/html/images/remotesensing-10-00527-g001.png" alt="drawing" width="600"/>
## Table of Contents
- [Overview of Data Fusion](#overview-of-data-fusion)
  - [Trends](#trends)
  - [Basic Concept](#basic-concept)
  - [Sensors](#sensors)
- [Focus, Taxonomy](#focus-taxonomy)
  - [Research Focus](#research-focus)
    - [1. Resolution enhancement:](#1-resolution-enhancement)
    - [2. Feature/object detection:](#2-featureobject-detection)
    - [3. Data Alignment.](#3-data-alignment)
  - [Taxonomy](#taxonomy)
- [Current Challengings](#current-challengings)
  - [1.  Issues Related to Radiation](#1--issues-related-to-radiation)
  - [2. Issues related to Topology](#2-issues-related-to-topology)
  - [3. Issues Related to Data](#3-issues-related-to-data)
  - [4.  Issues Related to Method and Process](#4--issues-related-to-method-and-process)
  - [5. Issues related to Physics](#5-issues-related-to-physics)
- [Algorithms](#algorithms)
  - [1.Spatial Resolution Enhancement Algorithms](#1spatial-resolution-enhancement-algorithms)
  - [2. Spatiotemporal Fusion by Traditional Methods](#2-spatiotemporal-fusion-by-traditional-methods)
  - [3. Spatio-Temporal Fusion by Nerual Network](#3-spatio-temporal-fusion-by-nerual-network)
  - [4.  SAR to Optical](#4--sar-to-optical)
  - [5.Registration](#5registration)
  - [6. Super Resolution Enhancement](#6-super-resolution-enhancement)
  - [7. Classification](#7-classification)
  - [8.Change Detction](#8change-detction)
- [Quality Assessment](#quality-assessment)
  - [1.Assessment Index With Reference Images.](#1assessment-index-with-reference-images)
  - [2.Assessment Index Without Reference Images.](#2assessment-index-without-reference-images)
- [Community](#community)
  - [IEEE GRSS data fusion contest](#ieee-grss-data-fusion-contestlinkhttpwwwgrss-ieeeorggrss-webinars)
  - [Discussion](#discussion)
- [Special Issue "Multisensor Data Fusion in Remote Sensing, 2018](#--special-issue-multisensor-data-fusion-in-remote-sensing-2018httpswwwmdpicomjournalremotesensingspecial_issuesmsdf_rs)
  - [Software and Open Source Tool](#software-and-open-source-tool)
    - [Cloud Services](#cloud-services)
    - [Useful Library](#useful-library)
  - [Database](#database)
- [TERMS](#terms)

## Overview of Data Fusion

### Trends
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
- [Remote Sensing Image Scene Classification Meets Deep Learning: Challenges, Methods, Benchmarks, and Opportunities](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/9127795)

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

## Focus, Taxonomy

### Research Focus
The application of data fusion in remote sensing is mainly divided in two scenarios:

#### 1. Resolution enhancement: 
It aims to provide higher resolution by combining multi modal data. The results are more like to be transition data, base map, or continuous time series for applications need high temporal and spatial resolution. 

They are mostly:
- Based on pixel level.
- Focus on Robustness, temporal  continuous 

For examples:
| Sub Topic | Enhancement  | Applications
|--|--|--|
| Super Resolution | Spatial | Transition for registration, base map
| pan-sharpening | Spatial  | base map 
| spatio-temporal fusion | Temporal and Spatial  | base map, time series

Typical applications: Plant detection, weather detection, ecology, change detection, land cover, etc.

#### 2. Feature/object detection: 
It aims to improve accuracy and precision of specific task, based on complementary property of heterogeneous information in multimodality. Often, temporal continuity can be sacrificed.

They are mostly:
- End to End 
-  based on pixel level or decision level.
- Focus on accuracy of task (instead of fused images)

For examples:

| Sub Topic | Enhancement  | Application
|--|--|--|
| Change detection | Accuracy of Change map | Land cover, Building..
| Object detection | Accuracy of Detection | Car, Building
| segmentation | Accuracy of Classification | Land Cover, Forest

Typical Applications:  change detection, land change coverage, land classification, disaster monitoring, building recognition, vehicle recognition, etc.

#### 3. Data Alignment.
It aims to find and adjust the unlinear connections between different sensors, It could be divided into matching and co-registration, Furthermore, the problems need to be resolved could be regarded as topological and radiation issues.
They are mostly:
- Necessary for all multi-modal applications
- part of preprocess
- can be selectively ignored or modified(such as adaptive registration)

For examples:
| Sub Topic |  Description
|--|--|--|
| Radiometric Correction |Atmospheric effect. etc
| Geometric Correction | Camera, Solar Angle etc
| Band Adjustment| Function based on prior knowledge
| BRDF Adjustment| Function based on vegetation
| Registration of Different Modal| SAR-Optical, Multi-Temporal..
| Adaptive Registration  | Domain, Manifold, Attention Mechanics, Tensor

### Taxonomy
*Depending on the main problem solved by the model/algorithm,  the development of data fusion can be divided into many areas*

- **According to process levels:** Pixel, Attribute, Decision
- **According to Principle:** Weighted function based, Decomposition  based, Learning based (including sparse dictionary,DL), Bayesian based, Hybrid based 
- **According to modal:** Homogeneous fusion, Heterogeneous fusion (NIR,-VIS, Optical-SAR, Optical-Thermal, hyper-Multi etc.,), Remote sensing site fusion, Remote sensing non-observation fusion (Data assimilation)
- **According to mechanisms:** Competitive integration, Complementary integration(like temporal and spatial), Cooperative integration(like 3D reconstruction)
- **According to Dimension**: Spatial Dimension Enhancement, Spectral Dimension Enhancement, Time dimension enhancement, End to End.
- **According to Applications**: spatial resolution enhancement , Matching and co-registration of multisource data,  Change detection, Object recognition, Agriculture, Ecology etc.,
- **According to procedure:** Matching, Co-registration, Process, Quality Assessment.


## Current Challengings
*In almost every small direction (as shown in the previous subsection). There are a number of issues so authors only list some most important challenges to demostrate.*

As metioned before, spatial enhancement and fusion of complimentary information are main scientific focus. Apart from these, there are: 

### 1.  Issues Related to Radiation 
| Issues| Popular Solutions | Description
|--|--|--|
|  Atmospheric effect   | Radiometric Correction | Commonsense
|  Solar azimuth and elevation  | Radiometric Correction |Commonsense
|  Band pass Adjustment  | linear regression |The small differences between MSI and OLI equivalent spectral bands need to be adjusted.
|  Bidirectional Reflectance Distribution effect  | BRD Function (BRDF) |The BRDF is needed in remote sensing for the correction of view and illumination angle effects (for example in image standardization and mosaicking)

###  2. Issues related to Topology
| Issues| Popular Solutions | Description
|--|--|--|
|  Lens Distortion| (Camera Calibration in) Geometric Correction | Commonsense
|  Error caused by Elevation(SAR and optical) | Co-Registration  | Please see figure1 and figure2
|  Mis-matching in pixel | Co-Registration | in Multi-Temporal, Multi-Sensor, Multi-Angle
|  Mis-matching in Feature | Co-Registration , Domain Adaptation| adaptive alignment as part of model
 |  Mis-matching in Object| Co-Registration , Attention Mechanics | adaptive alignment as part of model


Figure1. Error due to deviation in DEM, Relationship between error and Angle

![enter image description here](https://github.com/px39n/Awesome-Data-Fusion-for-Remote-Sensing/blob/main/imgs/relationship.png?raw=true)

###3. Issues Related to Data 
**Noise:** 
| Issues| Popular Solutions | Description
|--|--|--|
|  Noise in SAR | (Camera Calibration in) Geometric Correction | Speckle
|  Cloud | mask, super resolution, reconstruction, interpolation | 

**Sample:** 
| Issues| Popular Solutions | Description
|--|--|--|
|  Spectral/Index Colinearity, Similarity | PCA, Correlation Anlysis | Huges Phenomenon, Statistics
|  Lack of Samples | Data Augmentation, Semi-supervised, GANs | Overfitting, low generalization 
| Unbalanced Samples | Loss functions, updating... | weak train in small class 
 |  Gap in Resolution| Transition(Super resolution) | For 1:2 or higher resolution ratio in multi modal, It will increase the difficulty in data fusion
 
### 4.  Issues Related to Method and Process 
| Issues| Popular Solutions | Description
|--|--|--|
|  Computation Speed  | Alternative method, cloud service,Parallel computing  |  
|  Issues related to training| AI tools | like overvitting, vanished gradient etc., 
|  Hard to fuse heterogeneity| Pixel(like unmixing), feature(like feature layers), decision level(like DT) | multi-modal
|  low Generalization | Data augmentation, Domain Adaptive, Pre-train  |   transferability 
|  lack of Interpretability| Combination with prior knowlege(Branch, Attention, feature layers,data assimilation )  |   Physics


### 5. Issues related to Physics
| Issues| Popular Solutions | Description
|--|--|--|
|  Intra-class Variation| (updating)| Small difference between different class
| Inter-class variation | (updating)| Large difference in same class
| Landscape Heterogeneity| Learning based method,(updating)| Variations in high resolution pixel.
| Change due to Landcover | Learning based method,(updating)| 
| Abrupt Change | Function related to time(updating)| disaster etc
| Seasonal Change | Function related to time(updating)|  vegetation


## Algorithms
There are currently more than 200 spatio-temporal models, so only part of baseline models or polular papers are included.

### 1.Spatial Resolution Enhancement Algorithms 
*Multisensor image fusion for spatial resolution enhancement such as pan-sharpening, multi/hyperspectral image fusion, and downscaling of multiresolution imagery*


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


###  2. Spatiotemporal Fusion by Traditional Methods 
*(Normally Prediction by fusing two high temporal and high spatial resolution sensors with correction,Multisensor and multimodal data fusion using a variety of sensors such as optical imaging, SAR, and LiDAR)*
|Sensor| Principle |Method | Paper | Code| Features | Registration 
|--|--|--|--|--|--|--|
| Landsat&MODIS| Weighted Function |STARFM|（[Gao et al.2006](https://ieeexplore.ieee.org/abstract/document/1661809)) |[Python](https://github.com/topics/starfm)
|+ |+  |STAARCH| ([Hilker et al.2009](https://www.sciencedirect.com/science/article/pii/S003442570900087X)) | Code | Cloud and Snow Cover
| +|+  |ESTARFM|([Zhu et al.2010](https://www.sciencedirect.com/science/article/pii/S0034425710001884)) | [IDL,Python](https://xiaolinzhu.weebly.com/open-source-code.html) |Enhancement in Heterogeneous region 
| MODIS&landsat| + |RWSTFM|([wang et al.2017](https://www.mdpi.com/2072-4292/9/10/990)) |Code | kriging Based
| 1MODIS,2landsat| + | Prediction Smooth Method|([Zhong et al.2018](https://www.mdpi.com/2072-4292/10/9/1371/htm)) |Code | abrupt change, phenology| Manual
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
   | 2Landsat&1MODIS| + |STFDCNN| [Song et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8291042)| Code| Transition Image
   | | + |DCSFTN| | Code|
 | | Hybrid|FSDAF| ([Zhu et al.2016](https://www.sciencedirect.com/science/article/pii/S0034425715302042))| Abrupt Change 
 | |+ |NDVI-LMGM| ([yu et al.2015](https://www.mdpi.com/2072-4292/7/6/`7865`/htm))| linear growth&unmixing
 |Two Time series| Others |STAIR| ([Luo et al.2015](https://www.sciencedirect.com/science/article/pii/S0034425718301998))| Difference, Cloud
 |Multi Time series| Others |STAIR2| ([Luo et al.2020](https://www.mdpi.com/2072-4292/12/19/3209/htm))| 

### 3. Spatio-Temporal Fusion by Nerual Network
|Registration|Modal|Process Level|Method | Paper | Code| Features
|--|--|--|--|--|--|--|
|Traditional |A(T1,T3), B(T2)|pixel|StfNet(Two Branch)| ([Liu,2019](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8693668)) | Code| Features
|Traditional|A1-3,B1,3|pixel|Super Resolution, weighted function| ([SONG, 2019](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8291042/citations?tabFilter=papers#citations))| Code| Features
|Traditional|A1-3,B1,3|pixelLevel|Super Resolution, weighted function| [Li,2019](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8898524) | Code| Features
|Traditional|A12,B1 |PIXEL|DMnet, concatenate| [lI 2020](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/9109314) | Code| Features
|Traditional|A12,B1 |PIXEL|CNN, concatenate| [Yin 2020](|Traditional|A1,B1 |PIXEL|DMnet, concatenate| [lI 2020](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/9109314) | Code| Features) | Code| Features

### 4.  SAR to Optical
|Task| Source | Method | Paper | Code| Features
|--|--|--|--|--|--|
| Pan-Sharpening| Low&High |CNN|[jin et al.2016](https://link.springer.com/article/10.1007/s11220-016-0135-6)|Code | Resolution enhancedment of MSS
| Pan-Sharpening| Low&High |CNN|[G Masi et al.2016](https://scholar.google.com/scholar?as_q=Pansharpening+by+convolutional+neural+networks&as_occt=title&hl=en&as_sdt=0%2C31)|Code | End-to-End
| SAR 2 Optical| SAR |GANs|[Reyes et al.2018](https://www.mdpi.com/2072-4292/11/17/2067/htm)|[Code](https://github.com/seongjunyun/CNN-with-Dual-Local-and-Global-Attention) | Feature Level, two Stream, semi-auto- Label
| SAR 2 Optical(Cloud removal)| SAR |DRN|[Meraner et al.2018](https://pubmed.ncbi.nlm.nih.gov/32747852/)|[Code](https://github.com/ameraner/dsen2-cr) | cloud removal
| SAR 2 Optical| SAR |sar2opt|[Toriya et al.2019](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8898605?denied=)|[Code]() |
| Growth Prediction| Multi |CNN|[Scarpa et al.2018](https://www.mdpi.com/2072-4292/10/2/236/htm)|[Code](https://github.com/antoniomazza88/SAR2NDVI_CNN) | pixel level, Sentinel,NDVI fusion and pixel fusion
| Growth Prediction| SAR&VNIR |Random Forest|[hECKEL et al.2020](https://www.mdpi.com/2072-4292/12/2/302/htm)|[Code]() | pixel level, Sentinel
### 5.Registration
|Learning|Modal|Process Level|Method | Paper | Code| Features
|--|--|--|--|--|--|--|
Registration and SR| Low&High |Deep Neural Network|[Y. Qu et al.2018](https://ieeexplore.ieee.org/document/8897135)|[Code](https://github.com/zhouyuanzxcv/Hyperspectral) | 
Registration| SAR&Optical |Deep Neural Network|[Mou 2017 et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7924548) | Patch-based
| Recognition| Hyper&SAR |Dual DCNN|[Lagrange et al.2018](https://arxiv.org/abs/1605.05462)|[Code](https://github.com/seongjunyun/CNN-with-Dual-Local-and-Global-Attention) | Feature Level, two Stream
| Recognition| Multi&SAR |Multi-TaskUNet|[JIAN et al.2019](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8554076)|[Code](https://github.com/seongjunyun/CNN-with-Dual-Local-and-Global-Attention) | Multi-Task(Edge, Biniary),xception
| Registration| Optical&SAR |Siamese|[Mou et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7924548)|[Code](https://github.com/seongjunyun/CNN-with-Dual-Local-and-Global-Attention) | Feature Level, two Stream, semi-auto- Label
| Registration| Optical&SAR |3 DNN|[Hughes et al.2020](https://www.sciencedirect.com/science/article/pii/S0924271620302598?via%3Dihub)|[Code]() | hot map, goodness
| Registration| Optical&SAR |Siamese& Gaussian pyramid coupling quadtree|[He et al.2018](https://www.mdpi.com/2072-4292/10/2/355)|[Code]() | Coarse-finer
| Registration| Optical&SAR |Pseudo-Siamese CNN|[Hughes et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8314449)|[Code]() |  
| Supervised| Optical&SAR | Siamese CNN|[Merk et al.2017](https://www.mdpi.com/2072-4292/9/6/586/htm)|[Code]() |  
 
### 6. Super Resolution Enhancement
|Registration|Modal|Process Level|Method | Paper | Code| Features
|--|--|--|--|--|--|--|
||CNN|[Yuan et al.2016](https://scholar.google.com/scholar?as_q=Pansharpening+by+convolutional+neural+networks&as_occt=title&hl=en&as_sdt=0%2C31)|[Code](https://github.com/junjun-jiang/Hyperspectral-Image-Super-Resolution-Benchmark) | End-to-End,Transfer Model from CV, hyperspectrum
||Low&High |Deep Residual Convolutional Neural Network|[Wang et al 2017](http://www.ict.griffith.edu.au/~junzhou/papers/C_ICIG_2017.pdf)|[Code](https://github.com/junjun-jiang/Hyperspectral-Image-Super-Resolution-Benchmark) | End-to-End,Transfer Model from CV, hyperspectrum
||Low&High |SSF-CNN|[X. Han et al 2018](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8451142)|[Code](https://github.com/junjun-jiang/Hyperspectral-Image-Super-Resolution-Benchmark) | End-to-End,Transfer Model from CV, hyperspectrum
|| Low&High |Deep Neural Network|[R. Dian et al.2017](https://drive.google.com/open?id=1FIyVL9c8jlDY3heEZ57nGvpSDZc0mkeT)|[Code](https://github.com/renweidian/DHSIS) | 
| |  Low&High |Sparse Dirichlet-Net|[Y. Qu et al.2018](https://arxiv.org/abs/1804.05042)|[Code](https://github.com/aicip/uSDN) | 
|| Low&High |Deep Neural Network|[Y. Qu et al.2018](https://arxiv.org/abs/1902.00301)|[Code](https://github.com/acecreamu/deep-hs-prior) | 
|| Low&High |Deep Neural Network|[Y. Qu et al.2020](https://www.mdpi.com/2072-4292/13/2/167/htm)|[Code](https://github.com/acecreamu/deep-hs-prior) | Chen
Mannual|HSI-MSI|patch-based,concatenation| Super Resolution| Low&High |Deep Neural Network|[Yang et al.2018](https://www.mdpi.com/2072-4292/10/5/800/htm)|[Code](https://github.com/acecreamu/deep-hs-prior) | Two branches

### 7. Classification

|Registration|Modal|Process Level|Method | Paper | Code| Features
|--|--|--|--|--|--|--|
| Classification| Multi ||CNN|[Lagrange et al.2018](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7326745)|[Code](https://github.com/acecreamu/deep-hs-prior) | Comparision of existing
| Classification| Multi ||FusioNet|[Hu et al.2017](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/7924565)|[Code](https://github.com/acecreamu/deep-hs-prior) | Feature Level, two Stream
| | Multi| |DeepNetsForEO|[Audebert et al.2017](https://link.springer.com/chapter/10.1007/978-3-319-54181-5_12ithub # Semantic Segmentation of Earth Observation Data Using Multimodal and)|[Code](https://github.com/nshaud/DeepNetsForEO/blob/master/legacy/README.md) | Feature Level, two Stream
| Classification| VNIR-DSM ||DeepUNet|[Audebert et al.2017](https://ieeexplore-ieee-org.proxy.library.cornell.edu/document/8486170)|[Code](https://github.com/nshaud/DeepNetsForEO/blob/master/legacy/README.md) | Channel Packing
| Manual| Sentinel2,Lansat8, OSM,etc,. |Pixel(Concatenation)|ResNet|[Qiu et al.2018](https://www.mdpi.com/2072-4292/10/10/1572)|| LCZ maps

### 8.Change Detction
|Modal| Method | Paper | Code| Features
|--|--|--|--|--|--|
|SAR1 (T1, T2)|Ratioing/log Ratioing|[Papers](https://ieeexplore.ieee.org/abstract/document/6257409)||
|SAR1 (T1, T2)|Small wavelet transform|([Bovolo,2005](https://scholar.google.com/scholar_lookup?title=A%20detail-preserving%20scale-driven%20approach%20to%20change%20detection%20in%20multitemporal%20SAR%20images&author=Bovolo,%20F.&author=Bruzzone,%20L.&publication_year=2005&journal=IEEE%20Trans.%20Geosci.%20Remote%20Sens.&volume=43&pages=2963%E2%80%932972&doi=10.1109/TGRS.2005.857987))|| Unsupervised
|SAR1 (T1, T2),SAR2 (T1, T2)| Markov|([Solarna,2018](https://www.mdpi.com/2072-4292/10/11/1671/htm#B9-remotesensing-10-01671))||Unsupervised
More Change detection research please refer to [Awesome Change Detection](https://github.com/wenhwu/awesome-remote-sensing-change-detection)


## Quality Assessment
### 1.Assessment Index With Reference Images.
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
### 2.Assessment Index Without Reference Images.
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
### Discussion
- [Special Issue "Multisensor Data Fusion in Remote Sensing, 2018"](https://www.mdpi.com/journal/remotesensing/special_issues/msdf_rs)
- 


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