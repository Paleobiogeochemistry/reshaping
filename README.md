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

4. Main radiocarbon data files (siamradven) (each file is one sediment core data organized as the followed)  --> A: depth model in cm (called cm), B: radiocarbon age in years (called age), C: calendar age in years before present (called cal.age), D: error calendar age in years before present (called cal.age.err), E: radiocarbon age benthic foraminifera (called proxy.14C), F: error radiocarbon age benthic foraminifera (called proxy.14C.age.err), G: Delta 14C in permil that was calculated using the equation of Adkins and Boyle., 1997 (called proxy.D14C), H: error Delta 14C in permil that was calculated using the equation of Adkins and Boyle., 1997 (called proxy.D14C.err), K: planktic foraminifera 14C age (called planktic.14C.age), L: error planktic foraminifera 14C age (called planktic.14C.age.err) 
  
>* cm	age	cal.age	cal.age.err	proxy.14C.age	proxy.14c.age.err	proxy.D14C	proxy.D14C.err	ref.	chro.meth	chro.meth.details	planktic.species	planktic.14C.age	planktic.14C.age.err	planktic.D14C	planktic.D14C.err	Delta.R	Delta.R.err	calib.method	atmos.D14C	atmos.D14C.err	atmos.14C.age	atmos.14C.age.err	D14C.bias.correct	D14C.bias.correct.err	sed.rate	DIC.D14C	DIC.D14C.err	DIC.D14C.age	DIC.D14C.age.err	DELTA14Cage.atmos.RAW	DELTA14Cage.atmos.RAW.err	DELTA14Cage.atmos	DELTA14Cage.atmoserr	
>* 202	9354	9354	131	9340	20	-30.73498678	17.7733084	Fontaineetal.(2019)PP	3	NaN	Plankticsexistbutnotsamedepths—needtoinsert	NaN	NaN	NaN	NaN	0	0	2	101.3	3.2	8320	23	-95	32	78.4	-148.4	5	1290	40	1020	30	1651	NaN	
>* 218	9558	9558	137	9775	20	-58.88733094	17.94023942	Fontaineetal.(2019)PP	3	NaN	Plankticsexistbutnotsamedepths—needtoinsert	NaN	NaN	NaN	NaN	0	0	2	76.7	2.8	8696	21	-123	32	58.8	-148.4	5	1290	40	1079	29	1710	NaN	
>* 234	9830	9830	156	9990	20	-53.09367674	20.22739717	Fontaineetal.(2019)PP	3	NaN	Plankticsexistbutnotsamedepths—needtoinsert	NaN	NaN	NaN	NaN	0	0	2	96.3	3	8813	22	-117	33	56.1	-148.4	5	1290	40	1177	30	1808	NaN	
>* 250	10115	10115	153	10360	20	-64.00083659	19.65466361	Fontaineetal.(2019)PP	3	NaN	Plankticsexistbutnotsamedepths—needtoinsert	NaN	NaN	NaN	NaN	0	0	2	125.1	3.1	8887	22	-128	33	47.7	-148.4	5	1290	40	1473	30	2104	NaN	
>* 268	10492	10492	170	10600	20	-49.16473541	21.92194333	Fontaineetal.(2019)PP	3	NaN	Plankticsexistbutnotsamedepths—needtoinsert	NaN	NaN	NaN	NaN	0	0	2	120.9	3.2	9286	23	-113	35	49.4	-148.4	5	1290	40	1314	30	1945	NaN	
>* 292	10978	10978	165	10845	30	-21.88271569	23.1771584	Fontaineetal.(2019)PP	3	NaN	Plankticsexistbutnotsamedepths—needtoinsert	NaN	NaN	NaN	NaN	0	0	2	152.5	3.2	9529	22	-86	35	50.4	-148.4	5	1290	40	1316	37	1947	NaN	
>* 310	11335	11335	172	11480	20	-56.3414409	21.98483768	Fontaineetal.(2019)PP	3	NaN	Plankticsexistbutnotsamedepths—needtoinsert	NaN	NaN	NaN	NaN	0	0	2	140.8	3.4	9961	24	-121	35	49.8	-148.4	5	1290	40	1519	31	2150	NaN	
>* 321	11556	11556	172	11300	55	-8.811461828	27.41220516	Fontaineetal.(2019)PP	3	NaN	Plankticsexistbutnotsamedepths—needtoinsert	NaN	NaN	NaN	NaN	0	0	2	162.3	3.2	10025	22	-73	38	51.5	-148.4	5	1290	40	1275	59	1906	NaN	![image](https://github.com/user-attachments/assets/e727acd4-54ed-4115-9c33-b9861a85421e)

  







  
9. radiocarbon age planktonic foraminifera, G: radiocarbon age benthic foraminifera, E: diference of planktic and benthic foraminifera radiocarbon (ventilation age), F: , G: Delta 14C in per mil calculated of DeVries (2014) biogeochemical model, H: Diference between Column F and G (F-G).

Example siamradven files 




 
## Run the BOTcode (Generation of output file)

1) Install Python (recommendable last edition) https://www.python.org/
2) Check BOTcode (attached) 
3) Create in your PC a single folder where you add all imput files: sediment stations, hydrological parameter 1 (e.g., oxygen), hydrologial parameter 2 (e.g., temperatature), Hydrological parameter 3,4,5,6,n; BOTcode python.
4) Run the code
