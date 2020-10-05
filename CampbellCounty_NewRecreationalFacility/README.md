## Introduction:
To help county officials determine a site for a new recreational facility, I created a geospatial analysis of Campbell County, Virginia. The type of park that we are creating is a recreational park that is suitable for casual walking, exercising, picnicking, and enjoying nature. Campbell County is a suitable county for a new recreational park because it has slight elevation, plenty of streams and ponds, and a lot of open land.
## Study Area:
Campbell County is located in south central Virginia, and borders the Blue Ridge Mountains. The county study area comprises of thirty-seven census block groups, which is the primary unit of analysis for this project. The variables that determine which block group is the most suitable for a new recreational park are: 

•**Terrain/Slope** – This helps determine where land may not be developed for future use due to the steep slopes and rougher terrain. The steepness of slopes provides possible hiking and walking trails for public enjoyment. 

•**Waterbodies** – The suitable block group should comprise of high amounts of waterbodies such as streams and ponds. This provides a scenic attribute for hiking, picnicking, and enjoying nature. 

•**Land Cover** – This factor helps determine which block group has the desired type of land for a new recreational park. Block groups with developed land or with agriculture usage is less desirable, while block groups with open water, forests, and wetlands are perfect. The forests provide a aesthetic attribute to the location so it is a relaxing location for picnicking and exercising. 

•**Roads** – This factor provides the information where the possible location of the park is not compromised by roads and it is a scenic journey to the park. A lot of roads will produce traffic and make the park not as relaxing.

•**Population** – This factor helps determine the suitable block group by showing where the county population resides so that the park does not disturb or misplace any communities, but rather it adds to the experience of the county. 

•**Existing Parks** – This factor helps determine suitable block groups by showing where parks already exist so the new park does not go there. The new park is not meant to override other established places, it is supposed to add to the beauty of the county. 

•**Buildings** – This factor helps determine suitable block groups by providing the location of buildings, including homes and others, to make sure the possible locations of the parks do not have already established buildings so no history, or homes are taken by this park. This factor also helps fill in any gaps that the population factor might have missed.
## Methods
In order to determine the suitable block group for the new recreational park in Campbell County, Virginia, I took all of the factors above and calculated the slope mean, landcover mean, population density, roads density, waterbody density (linear and area), building density, and existing park density. To determine a block groups density for each factor I calculated the length of each factor and divided that by the area of the block group. Then, I standardized all scores by using this equation: (value-minimum value)/(maximum value/minimum value)*100. The standardization equation allowed me to have each factor score range from zero to one-hundred, the minimum value being zero, and the maximum being one-hundred. I then calculated the weighted score for every factor using the following weights: Slope Mean 13% or 0.13, Landcover 18% or .18, Linear Water	10% or 0.1, Area Water 10% or 0.1, Road Density 10% or 0.1, Population Density 13% or 0.13, Building Density 13% or 0.13, and Parks Density 13% or 0.13. Landcover is the highest because the type of land is the most important factor since it tells us which block group has a higher composition of preferable land. Population Density, Park Density, Slope Mean, and Building Density hold the second highest weight because they contribute to further selection of the park site. Building density and population density are similar in the purpose of the data, however, there are buildings that are not residential and I did not want to tear down anything especially if it holds any historical value to the county. Park density is important because I did not want to have the new park overlapping a current one. Linear Water, Area Water, and Road Density hold the lowest weight because I think they hold aesthetic attributes, which are important, however I weighted them less since the other factors could cost someone their home. Aesthetics are only as good as they look if no one was hurt or lost something while getting the land. 
## Site Suggestion
The following map provides the location of the most suitable block group along with the second and third alternatives, the map also shows the less suitable block groups, those who did not rank in the top 20 following the weight calculations for all factors. 
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/SuitableBlockGroups.png">
</p>
The names of the top three block groups are as follows: Most Suitable – 510310204031, Second Suitable – 510310206002, and Third Suitable – 510310201012. The Most Suitable block group was the highest ranked group after standardization and after weighing the factors.  Its Weighted Slope Mean is 12.22729, Weighted Landcover 17.85176, Weighted Roads 9.381245, Weighted Linear Water 5.051507, Weighted Area Water 0.281956, Weighted Park Density 13, Weighted Building Density 12.4449, Weighted Population Density 12.51852, and Weighted Total 82.75718.
The following table provides the scores of the top 20 block groups after I standardized their scores for each factor using this equation: (value-minimum value)/(maximum value/minimum value)*100. I then totaled the standardized scores for each block group to determine the highest twenty ranking block groups:
| Rank | GEOID | Slope Mean Standardized | Landcover Standardized | Roads Standardized | LinearWater Standardized | AreaWater Standardized	| Parks Standardized | Buildings Standardized	| Population Standardized | Total Standardized |

| 1 | 510310204031 | 94.05607	| 99.17646 | 93.81245	| 50.51507 | 2.819563	| 100	| 95.73001 | 96.2963 | 632.4059 |
| 2	| 510310206002 | 93.05731 |	95.68336 | 94.54916	| 47.76803 | 6.044126	| 100	| 97.20199 |97.82886 | 632.1328 |
3	510310201012	100	93.32192	90.02312	57.87867	2.252565	100	93.15718	94.5083	631.1418
4	510310206003	84.55407	99.17172	98.15432	45.70775	2.520636	100	98.09852	98.72286	626.9299
5	510310201013	86.81889	95.19106	91.09291	40.55704	1.193782	100	93.78266	95.4023	604.0386
6	510310205002	70.61241	97.19177	92.13527	46.01297	0.291213	100	93.87301	95.91315	596.0298
7	510310208003	65.05135	98.02177	100	17.28348	1.812852	98.43283	99.46069	99.61686	579.6798
8	510310209001	61.65998	99.49662	99.73745	16.86379	0.0945	100	100	100	577.8523
9	510310206001	65.74959	98.19885	94.89792	16.02442	7.235979	100	97.47581	97.70115	577.2837
10	510310209002	69.98097	95.70724	96.47713	12.24723	2.559207	100	97.98871	98.97829	573.9388
11	510310201021	57.68606	99.12256	97.80948	20.52652	0	100	97.82331	98.33972	571.3076
12	510310201022	64.12126	99.4083	96.10486	17.70317	0	97.9543	96.17202	97.06258	568.5265
13	510310202001	37.46963	100	95.68949	43.87638	0.428142	100	95.1629	95.65773	568.2843
14	510310208001	61.20937	98.55678	96.72009	13.31553	0.075214	100	98.42238	98.97829	567.2777
15	510310201011	43.2737	98.24318	93.8438	39.41244	0.219857	100	95.67163	96.2963	566.9609
16	510310209003	84.74966	83.84326	87.66409	18.96223	25.91414	92.60677	84.01813	88.88889	566.6472
17	510310208002	49.98841	98.56044	97.19033	20.10683	0	100	99.71367	99.74457	565.3042
18	510310204034	33.25915	97.44545	90.81469	33.00267	0.239142	100	88.11437	93.86973	536.7452
19	510310205003	36.55004	95.25378	85.70477	36.93247	0.391499	100	89.40565	91.95402	536.1922
20	510310207003	67.52139	58.49585	66.47204	50.20984	50.1755	96.69817	69.02591	75.35121	533.9499