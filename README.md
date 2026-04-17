# replication_code_JEEM_anemia
notebooks needed to replicate the JEEM-D-25-00707

Before running the code blocks, you need to download or register to access the following datasets :

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


