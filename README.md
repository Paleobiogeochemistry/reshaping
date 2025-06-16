### reshaping

## A tool for fast time interval (years before present) proxy data analysis for large data sediment core data bases. 

# Motivation and scientific goals

This GitHub repository storage all codes used for data analysis and visualization of the stable isotopes and radiocarbon ventilation ages (can be used for any other proxy data) results for the work "Reshaping the Southeast Pacific Water Masses since the Last Glacial - Interglacial transition: Dynamics and Carbon Storage".

We used for published data mining and the organization of our new stable isotope and radiocarbon data the methodology described by Muglia et al., 2023 (https://www.nature.com/articles/s41597-023-02024-2) that consider the organization of depth model, age data raw data and age model and proxy data per sediment core in indivialds folders with notes about the data update and mangment. A soon the new data will be published, will be submited to Muglia et al., 2024 (https://zenodo.org/records/11187264)  For the most updated versions of the data set, each core information was organized in two txt files.  

## Getting started (Generation of proxy data sediment sites imput files)  

1. Main metadata file: This file (called index) will storage all metada information of the sediment cores that will be analyzed. Mandatory information is the location [(longitude (in degress east), latitude (in degress north), water depth (in meters bellow the sea level)] and the ID of the core. The text file is separated by tabulations without spaces. In relation to the ID of the core, the first part of the name represent the type of analysis, the second part the name of the core.
siamrad: represent the cores with results used for d13C and d18O data analysis and visualization. 
siamradven: represent the cores with results used for radiocarbon ventilation ages data analysis and visualization. 

   Example of index siamrad  

>*IDarchive	longitude	latitude	depth
>*siamrad_so26_96	-85.84	0.68	2706
>*siamrad_so26_127	-85.39	-1.55	2463
>*siamrad_so26_131	-85.00	-3.53	3381
>*siamrad_gik17747_1	-72.33	-32.74	2464
>*siamrad_geob3302_1	-72.09	-33.22	1498

   Example of index siamradven  

>*site	longitude	latitude	depth
>*siamradven_md07_3088	-75.00	-46.00	1536.00
>*siamradven_geob7167_6	-73.93	-36.45	2062.00
>*siamradven_22sl	-73.68	-36.22	1001.00
>*siamradven_geob7163_7	-73.60	-36.43	537.00
>*siamradven_geob7149_2	-72.00	-31.49	3086.00

  
3. For stable isotope data --> A: cm (depth model), B: age in years before present (age model), C: carbon stable isotopes in benthic foraminifera d13C, D: oxygen stable isotope in benthic foraminifera d18O.
4. For radiocarbon data --> A: cm (depth model), B: age in years before present (age model), C: radiocarbon age planktonic foraminifera, D: radiocarbon age benthic foraminifera, E: diference of planktic and benthic foraminifera radiocarbon (ventilation age), F: Delta 14C in permil that was calculated using the equation of Adkins and Boyle., 1997, G: Delta 14C in per mil calculated of DeVries (2014) biogeochemical model, H: Diference between Column F and G (F-G).
 

