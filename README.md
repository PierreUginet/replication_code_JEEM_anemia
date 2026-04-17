# replication_code_JEEM_anemia
This Gihub repo provides instructions and notebooks needed to replicate the JEEM-D-25-00707.
Before runnnig any script, the following steps should be completed.

## Raw Datasets

Before running the notebooks, you need to download or register to access the following datasets :

### DHS data 

The National Family Health survey data are publicly available from the U.S. Department of Homeland Security (DHS) and can be accessed through its official data platforms following a standard user registration process. Researchers are required to create an account on the DHS data portal to obtain access to the datasets. Once registered, the data can be freely downloaded in accordance with DHS terms of use, including any applicable attribution and data protection requirements.

The 2015 datasets are listed on https://dhsprogram.com/data/dataset/India_Standard-DHS_2015.cfm?flag=0

The 2019-21 datasets are listed on https://dhsprogram.com/data/dataset/India_Standard-DHS_2020.cfm?flag=1

For replicating the analysis, the following datasets have to be downloaded and extracted to the corresponding folder/path:
* 2015 Children's Recode: IAKR74DT.ZIP (85.6 MB	Stata dataset) to
  * 0_input/DHS_data/input/IA_2015-16_DHS/IAKR74DT_Children_Stata/IAKR74FL.DTA
* 2015 Individual (Women) Recode: IAIR74DT.ZIP (326 MB, Stata dataset) to
  * 0_input/DHS_data/input/IA_2015-16_DHS/IAIR74DT_Women_Stata/IAIR74FL.DTA
* 2015 Men's Recode: IAMR74DT.ZIP (21.2 MB, Stata dataset) to
  * 0_input/DHS_data/input/IA_2015-16_DHS/IAMR74DT_Men_Stata/IAMR74FL.DTA
* 2015 Household Member Recode: IAPR74DT.ZIP (180 MB, Stata dataset) to
  * 0_input/DHS_data/input/IA_2015-16_DHS/IAPR74DT_HHmembers_Stata/IAPR74FL.DTA 
* 2015 Geographic Data: IAGE71FL.ZIP (2.31 MB, Shape file) to
  * 0_input/DHS_data/input/IA_2015-16_DHS/IAGE71FL_GeoData_shp/IAGE71FL.shp

* 2019 Children's Recode: IAKR7EDT.ZIP	(81.0 MB, Stata dataset) to
  * 0_input/DHS_data/input/IA_2019-21_DHS/IAKR7EDT_Children_Stata/IAKR7DFL.DTA
* 2019 Individual (Women) Recode: IAIR7EDT.ZIP (376 MB, Stata dataset) to
  * 0_input/DHS_data/input/IA_2019-21_DHS/IAIR7EDT_Women_Stata/IAIR7EFL.DTA
* 2019 Men's Recode: IAMR7E.ZIP	(23.0 MB, Stata dataset) to
  * 0_input/DHS_data/input/IA_2019-21_DHS/IAMR7EDT_Men_Stata/IAMR7EFL.DTA
* 2019 Household Member Recode: IAPR7EDT.ZIP (233 MB Stata dataset) to
  * 0_input/DHS_data/input/IA_2019-21_DHS/IAPR7EDT_HHmembers_Stata/IAPR7EFL.DTA 
* 2019 Geographic Data: IAGE7AFL.ZIP (2.21 MB, Shape file) to
  * 0_input/DHS_data/input/IA_2019-21_DHS/IAGE7AFL_GeoData_shp/IAGE7AFL.shp

### ERA5 data
The climate data are publicly available from de Climate Data Store (CDS). Although they can be downloaded manually, we provide a script that automatically download the required data using the CDS API. To use this script properly, one should follow the instruction provided by the Copernicus CDS that can be found on the following link. https://cds.climate.copernicus.eu/how-to-api

### Malaria data
The data on Annual Paratistic Incidence (API) at district level are available on the following link. We use data from 2018.
[https://ncvbdc.mohfw.gov.in/Doc/Annual-Report-2018.pdf](https://ncvbdc.mohfw.gov.in/index1.php?lang=1&level=1&sublinkid=5784&lid=3689)


## Code structure

In each folder, the files being used in the following stages are in the *output* folder. The files being intermediaries within each stage are in the *interm* folder.


## Dependencies

### Python requirements
All package required are stored in file python_requirement.txt 
The whole list of packages can be installed directly using pip install -r requirements.txt

### R sessionInfo()
R version 4.4.3 (2025-02-28)
Platform: x86_64-conda-linux-gnu
Running under: CentOS Stream 9

Matrix products: default
BLAS/LAPACK: /data/software/mambaforge/mambaforge/envs/R_HeatAnemia/lib/libopenblasp-r0.3.30.so;  LAPACK version 3.12.0

locale:
 [1] LC_CTYPE=fr_FR.UTF-8       LC_NUMERIC=C              
 [3] LC_TIME=fr_FR.UTF-8        LC_COLLATE=fr_FR.UTF-8    
 [5] LC_MONETARY=fr_FR.UTF-8    LC_MESSAGES=fr_FR.UTF-8   
 [7] LC_PAPER=fr_FR.UTF-8       LC_NAME=C                 
 [9] LC_ADDRESS=C               LC_TELEPHONE=C            
[11] LC_MEASUREMENT=fr_FR.UTF-8 LC_IDENTIFICATION=C       

time zone: Europe/Paris
tzcode source: system (glibc)

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] sf_1.1-0          terra_1.9-1       viridis_0.6.5     viridisLite_0.4.3
 [5] data.table_1.17.8 ggpubr_0.6.3      patchwork_1.3.2   stargazer_5.2.3  
 [9] ggfixest_0.4.0    fixest_0.14.0     lubridate_1.9.5   forcats_1.0.1    
[13] stringr_1.6.0     dplyr_1.2.0       purrr_1.2.1       readr_2.2.0      
[17] tidyr_1.3.2       tibble_3.3.1      ggplot2_4.0.2     tidyverse_2.0.0  

loaded via a namespace (and not attached):
 [1] gtable_0.3.6           rstatix_0.7.3          lattice_0.22-9        
 [4] tzdb_0.5.0             numDeriv_2016.8-1.1    vctrs_0.7.2           
 [7] tools_4.4.3            generics_0.1.4         sandwich_3.1-1        
[10] proxy_0.4-29           pkgconfig_2.0.3        KernSmooth_2.23-26    
[13] RColorBrewer_1.1-3     S7_0.2.1               stringmagic_1.2.0     
[16] uuid_1.2-2             lifecycle_1.0.5        compiler_4.4.3        
[19] farver_2.1.2           textshaping_1.0.5      repr_1.1.7            
[22] codetools_0.2-20       getPass_0.2-4          carData_3.0-6         
[25] class_7.3-23           htmltools_0.5.9        marginaleffects_0.32.0
[28] Formula_1.2-5          pillar_1.11.1          car_3.1-5             
[31] crayon_1.5.3           classInt_0.4-11        abind_1.4-8           
[34] nlme_3.1-168           tidyselect_1.2.1       digest_0.6.39         
[37] stringi_1.8.7          fastmap_1.2.0          grid_4.4.3            
[40] cli_3.6.5              magrittr_2.0.4         base64enc_0.1-6       
[43] dichromat_2.0-0.1      e1071_1.7-17           IRdisplay_1.1         
[46] broom_1.0.12           withr_3.0.2            dreamerr_1.4.0        
[49] scales_1.4.0           backports_1.5.0        IRkernel_1.3.2        
[52] timechange_0.4.0       otel_0.2.0             gridExtra_2.3         
[55] pbdZMQ_0.3-14          ggsignif_0.6.4         ragg_1.5.2            
[58] zoo_1.8-15             hms_1.1.4              evaluate_1.0.5        
[61] rlang_1.1.7            Rcpp_1.1.1             DBI_1.3.0             
[64] glue_1.8.0             jsonlite_2.0.0         R6_2.6.1              
[67] units_1.0-1            systemfonts_1.3.2 

