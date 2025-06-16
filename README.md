# reshape (under edition)

# A tool for fast time interval (years before present) proxy data analysis for large data sediment core data bases. 

## Motivation and scientific goals

This GitHub repository storage all codes used for data analysis and visualization of the stable isotopes and radiocarbon ventilation ages (can be used for any other proxy data) results for the work "Reshaping the Southeast Pacific Water Masses since the Last Glacial - Interglacial transition: Dynamics and Carbon Storage".

We used for published data mining and the organization of our new stable isotope and radiocarbon data the methodology described by Muglia et al., 2023 (https://www.nature.com/articles/s41597-023-02024-2) that consider the organization of depth model, age data raw data and age model and proxy data per sediment core in indivialds folders with notes about the data update and mangment. A soon the new data will be published, will be submited to Muglia et al., 2024 (https://zenodo.org/records/11187264)  For the most updated versions of the data set, each core information was organized in two txt files.  



## Getting started (Generation of proxy data sediment sites imput files)  

1. Main metadata file: This file (called index) will storage all metada information of the sediment cores that will be analyzed. Mandatory information is the location [(longitude (in degress east), latitude (in degress north), water depth (in meters bellow the sea level)] and the ID of the core. The text file is separated by tabulations without spaces. In relation to the ID of the core, the first part of the name represent the type of analysis, the second part the name of the core.

>* siamrad: represent the cores with results used for d13C and d18O data analysis and visualization. 
>* siamradven: represent the cores with results used for radiocarbon ventilation ages data analysis and visualization. 

   Example of index siamrad  

>* IDarchive	longitude	latitude	depth
>* siamrad_so26_96	-85.84	0.68	2706
>* siamrad_so26_127	-85.39	-1.55	2463
>* siamrad_so26_131	-85.00	-3.53	3381
>* siamrad_gik17747_1	-72.33	-32.74	2464
>* siamrad_geob3302_1	-72.09	-33.22	1498

   Example of index siamradven  

>* IDarchive	longitude	latitude	depth
>* siamradven_md07_3088	-75.00	-46.00	1536.00
>* siamradven_geob7167_6	-73.93	-36.45	2062.00
>* siamradven_22sl	-73.68	-36.22	1001.00
>* siamradven_geob7163_7	-73.60	-36.43	537.00
>* siamradven_geob7149_2	-72.00	-31.49	3086.00

  
2. Main stable isotope data files (siamrad) (each file is one sediment core data organized as the followed) --> A: cm (depth model), B: age in years before present (age model), C: carbon stable isotopes in benthic foraminifera d13C, D: oxygen stable isotope in benthic foraminifera d18O. 

Example siamrad files 

>* cm	age	d13C	d18O
>* 7	6500	0.02	2.8
>* 10	7543	-0.02	2.92
>* 12	8239	-0.09	3.16
>* 12	8413	0.09	2.84
>* 18	10500	0.01	3.22
>* 20	10947	0.07	3.37
>* 21	11158	-0.24	3.44
>* 21	11290	-0.01	3.46

4. Main radiocarbon data files (siamradven). Each file is one sediment core data organized following Rafter et al., 2022 https://www.science.org/doi/full/10.1126/sciadv.abq5434. 

A: depth model in cm (called cm)
B: radiocarbon age in years (called age)
C: calendar age in years before present (called cal.age)
D: error calendar age in years before present (called cal.age.err)
E: radiocarbon age benthic foraminifera (called proxy.14C)
F: error radiocarbon age benthic foraminifera (called proxy.14C.age.err)
G: Delta 14C in permil that was calculated using the equation of Adkins and Boyle., 1997 (called proxy.D14C)
H: error Delta 14C in permil that was calculated using the equation of Adkins and Boyle., 1997 (called proxy.D14C.err)
I: reference
J: planktic foraminifera 14C age (called planktic.14C.age)
K: error planktic foraminifera 14C age (called planktic.14C.age.err)
L: reservoir age (called Delta.R), M: error reservoir age (called Delta.R.err)
N: contemporany atmosphere D14C (atmos.D14C)
O: error contemporany atmosphere D14C (atmos.D14C.err)
P: atmosphere atmos.14C.age
Q: contemporany atmosphere 14C (called atmos.14C.age.err)
R: contemporany atmosphere 14C (called D14C.bias.correct)
S: (called D14C.bias.correct.err)
T: (called DIC.D14C) 
U: DIC.D14C.err
V: DIC.D14C.age
W: DIC.D14C.age.err
X: DELTA14Cage.atmos.RAW
Y: DELTA14Cage.atmos.RAW.err
Z: DELTA14Cage.atmos
AA: DELTA14Cage.atmos.err

![image](https://github.com/user-attachments/assets/ae686300-d92e-414f-af42-35eb2714d23d)

5. Surface sediment data (If you want to include this data)

6. Modern Bottom water hydrological variables (in this case d13C and d18O equilibrium calcite) 
 
## What each code do? 

1. water_mass_plot.py

Several plots using the following variables latitude, longitude, water depth versus d13C, d18O, Radiocarbon ventilation ages





3. (add name).py






4. (add name).py

## Run reshape python codes (Generation of output file)

1) Install Python (recommendable last edition) https://www.python.org/
2) Check reshape codes 1, 2, 3 (attached) 
3) Create in your PC a single folder where you add all imput files: index, siamrad core sites, siamradven core sites, surface sediments siamrad core sites (only one file per list), bottom water d13C and d18O (if are available)  
4) Run the code in your terminal or Spider console

## Data management and script developers 

* **Dharma A. Reyes Macaya** - [*Paleobiogeochemistry working group*](https://pastclimates.site.hw.ac.uk/)*, Lyell Centre, Heriot-Watt University, Scotland, UK* - [*MARUM*](https://www.marum.de/en/index.html)*, University of Bremen, Germany* - [dharmisreyesmacaya@gmail.com] Marine Biogeochemist, Paleoceanographer and Data Scientist
* **Francisco Manuel García Araya** - [garcicia@gmail.com] Earth Scientist, Numerical Modeller, Python mentor. 

### reshape Collaborators

* **Consuelo Martínez Fontaine** - [consuelola.m.f@gmail.com]
* **Katya Canal Solis** - [*Paleobiogeochemistry working group*](https://pastclimates.site.hw.ac.uk/)*, Lyell Centre, Heriot-Watt University, Scotland, UK*
* **Babette Hoogakker** - [*Paleobiogeochemistry working group*](https://pastclimates.site.hw.ac.uk/)*, Lyell Centre, Heriot-Watt University, Scotland, UK*


