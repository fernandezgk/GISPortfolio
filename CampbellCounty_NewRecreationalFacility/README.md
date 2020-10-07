## Introduction:
To help county officials determine a site for a new recreational facility, I created a geospatial analysis of Campbell County, Virginia. The type of park that we are creating is a recreational park that is suitable for casual walking, exercising, picnicking, and enjoying nature. Campbell County is a suitable county for a new recreational park because it has slight elevation, plenty of streams and ponds, and a lot of open land.
## Study Area:
Campbell County is located in south central Virginia, and borders the Blue Ridge Mountains. The county study area comprises of thirty-seven census block groups, which is the primary unit of analysis for this project. The block group data was downloaded from the Census Data [website](https://data.census.gov/cedsci/). The variables that determine which block group is the most suitable for a new recreational park are: 

•**Terrain/Slope** – This helps determine where land may not be developed for future use due to the steep slopes and rougher terrain. The steepness of slopes provides possible hiking and walking trails for public enjoyment. 

•**Waterbodies** – The suitable block group should comprise of high amounts of waterbodies such as streams and ponds. This provides a scenic attribute for hiking, picnicking, and enjoying nature. 

•**Land Cover** – This factor helps determine which block group has the desired type of land for a new recreational park. Block groups with developed land or with agriculture usage is less desirable, while block groups with open water, forests, and wetlands are perfect. The forests provide a aesthetic attribute to the location so it is a relaxing location for picnicking and exercising. 

•**Roads** – This factor provides the information where the possible location of the park is not compromised by roads and it is a scenic journey to the park. A lot of roads will produce traffic and make the park not as relaxing.

•**Population** – This factor helps determine the suitable block group by showing where the county population resides so that the park does not disturb or misplace any communities, but rather it adds to the experience of the county. 

•**Existing Parks** – This factor helps determine suitable block groups by showing where parks already exist so the new park does not go there. The new park is not meant to override other established places, it is supposed to add to the beauty of the county. 

•**Buildings** – This factor helps determine suitable block groups by providing the location of buildings, including homes and others, to make sure the possible locations of the parks do not have already established buildings so no history, or homes are taken by this park. This factor also helps fill in any gaps that the population factor might have missed.
## Methods
In order to determine the suitable block group for the new recreational park in Campbell County, Virginia, I took all of the factors above and calculated the slope mean, landcover mean, population density, roads density, waterbody density (linear and area), building density, and existing park density. The terrain data was downloaded from the Geospatial Data Gateway [website](https://datagateway.nrcs.usda.gov/GDGOrder.aspx) in order to termine the slope mean of the block groups. The landcover data was downloaded from the Multi-Resolution Land Characteristics (MRLC) [website](https://www.mrlc.gov/data) and was used to determine the lancover mean. The population, roads, linear water, and area water data were downloaded from the Census Data [website](https://data.census.gov/cedsci/), and was used to determine the mean of the given attribute. The building and existing park data were downloaded from the Campbell County GIS website [here](https://data1-campbellva.hub.arcgis.com/search?tags=planimetrics) in order to determine the Parks Density and Buildings Density. 

To determine a block groups density for each factor I calculated the length of each factor and divided that by the area of the block group. Then, I standardized all scores by using this equation: (value-minimum value)/(maximum value/minimum value)*100. The standardization equation allowed me to have each factor score range from zero to one-hundred, the minimum value being zero, and the maximum being one-hundred. I then calculated the weighted score for every factor using the following weights: Slope Mean 13% or 0.13, Landcover 18% or .18, Linear Water	10% or 0.1, Area Water 10% or 0.1, Road Density 10% or 0.1, Population Density 13% or 0.13, Building Density 13% or 0.13, and Parks Density 13% or 0.13. Landcover is the highest because the type of land is the most important factor since it tells us which block group has a higher composition of preferable land. Population Density, Park Density, Slope Mean, and Building Density hold the second highest weight because they contribute to further selection of the park site. Building density and population density are similar in the purpose of the data, however, there are buildings that are not residential and I did not want to tear down anything especially if it holds any historical value to the county. Park density is important because I did not want to have the new park overlapping a current one. Linear Water, Area Water, and Road Density hold the lowest weight because I think they hold aesthetic attributes, which are important, however I weighted them less since the other factors could cost someone their home. Aesthetics are only as good as they look if no one was hurt or lost something while getting the land. 
## Site Suggestion
The following map provides the location of the most suitable block group along with the second and third alternatives, the map also shows the less suitable block groups, those who did not rank in the top 20 following the weight calculations for all factors. 
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/SuitableBlockGroups.png">
</p>

The names of the top three block groups are as follows: Most Suitable – 510310204031, Second Suitable – 510310206002, and Third Suitable – 510310201012. The Most Suitable block group was the highest ranked group after standardization and after weighing the factors.  Its Weighted Slope Mean is 12.22729, Weighted Landcover 17.85176, Weighted Roads 9.381245, Weighted Linear Water 5.051507, Weighted Area Water 0.281956, Weighted Park Density 13, Weighted Building Density 12.4449, Weighted Population Density 12.51852, and Weighted Total 82.75718.
The following table provides the scores of the top 20 block groups after I standardized their scores for each factor using this equation: (value-minimum value)/(maximum value/minimum value)*100. I then totaled the standardized scores for each block group to determine the highest twenty ranking block groups:

| Rank | GEOID | Slope Mean Standardized | Landcover Standardized | Roads Standardized | LinearWater Standardized | AreaWater Standardized | Parks Standardized | Buildings Standardized	| Population Standardized | Total Standardized |
| -- | ---- | ---------- | -------- | -------- | ---------- | ------ | --------- | -------- | ------- | -------- |
1|510310204031|94.05607|99.17646|93.81245|50.51507|2.819563|100|95.73001|96.2963|632.4059
2|510310206002|93.05731|95.68336|94.54916|47.76803|6.044126|100|97.20199|97.82886|632.1328
3|510310201012|100|93.32192|90.02312|57.87867|2.252565|100|93.15718|94.5083|631.1418
4|510310206003|84.55407|99.17172|98.15432|45.70775|2.520636|100|98.09852|98.72286|626.9299
5|510310201013|86.81889|95.19106|91.09291|40.55704|1.193782|100|93.78266|95.4023|604.0386
6|510310205002|70.61241|97.19177|92.13527|46.01297|0.291213|100|93.87301|95.91315|596.0298
7|510310208003|65.05135|98.02177|100|17.28348|1.812852|98.43283|99.46069|99.61686|579.6798
8|510310209001|61.65998|99.49662|99.73745|16.86379|0.0945|100|100|100|577.8523
9|510310206001|65.74959|98.19885|94.89792|16.02442|7.235979|100|97.47581|97.70115|577.2837
10|510310209002|69.98097|95.70724|96.47713|12.24723|2.559207|100|97.98871|98.97829|573.9388
11|510310201021|57.68606|99.12256|97.80948|20.52652|0|100|97.82331|98.33972|571.3076
12|510310201022|64.12126|99.4083|96.10486|17.70317|0|97.9543|96.17202|97.06258|568.5265
13|510310202001|37.46963|100|95.68949|43.87638|0.428142|100|95.1629|95.65773|568.2843
14|510310208001|61.20937|98.55678|96.72009|13.31553|0.075214|100|98.42238|98.97829|567.2777
15|510310201011|43.2737|98.24318|93.8438|39.41244|0.219857|100|95.67163|96.2963|566.9609
16|510310209003|84.74966|83.84326|87.66409|18.96223|25.91414|92.60677|84.01813|88.88889|566.6472
17|510310208002|49.98841|98.56044|97.19033|20.10683|0|100|99.71367|99.74457|565.3042
18|510310204034|33.25915|97.44545|90.81469|33.00267|0.239142|100|88.11437|93.86973|536.7452
19|510310205003|36.55004|95.25378|85.70477|36.93247|0.391499|100|89.40565|91.95402|536.1922
20|510310207003|67.52139|58.49585|66.47204|50.20984|50.1755|96.69817|69.02591|75.35121|533.9499

The following table provides the scores of the highest ranking 20 block groups after I weighted all standardized scores for each factor. The weights are again, Slope Mean 13% or 0.13, Landcover 18% or .18, Road Density 10% or 0.1, Linear Water 10% or 0.1, Area Water 10% or 0.1, Parks Density 13% or 0.13, Building Density 13% or 0.13, and Population Density 13% or 0.13. I then totaled the weighted scores for each block group to determine the highest twenty ranking block groups: 

| Rank | GEOID | Slope Mean Weighted | Landcover Weighted | Roads Weighted | LinearWater Weighted	| AreaWater Weighted | Parks Weighted	| Buildings Weighted | Population Weighted | Total Weighted | 
| -- | ---- | ---------- | -------- | -------- | ---------- | ------ | --------- | -------- | ------- | -------- | 
1|510310204031|12.22729|17.85176|9.381245|5.051507|0.281956|13|12.4449|12.51852|82.75718
2|510310206002|12.09745|17.223|9.454916|4.776803|0.604413|13|12.63626|12.71775|82.5106
3|510310201012|13|16.79795|9.002312|5.787867|0.225256|13|12.11043|12.28608|82.20989
4|510310206003|10.99203|17.85091|9.815432|4.570775|0.252064|13|12.75281|12.83397|82.06799
5|510310201013|11.28646|17.13439|9.109291|4.055704|0.119378|13|12.19175|12.4023|79.29927
6|510310205002|9.179613|17.49452|9.213527|4.601297|0.029121|13|12.20349|12.46871|78.19028
7|510310208003|8.456676|17.64392|10|1.728348|0.181285|12.79627|12.92989|12.95019|76.68658
8|510310209001|8.015798|17.90939|9.973745|1.686379|0.00945|13|13|13|76.59476
9|510310206001|8.547447|17.67579|9.489792|1.602442|0.723598|13|12.67186|12.70115|76.41208
10|510310209002|9.097526|17.2273|9.647713|1.224723|0.255921|13|12.73853|12.86718|76.0589
11|510310201021|7.499187|17.84206|9.780948|2.052652|0|13|12.71703|12.78416|75.67604
12|510310201022|8.335764|17.89349|9.610486|1.770317|0|12.73406|12.50236|12.61814|75.46462
13|510310208001|7.957219|17.74022|9.672009|1.331553|0.007521|13|12.79491|12.86718|75.37061
14|510310208002|6.498493|17.74088|9.719033|2.010683|0|13|12.96278|12.96679|74.89866
15|510310202001|4.871051|18|9.568949|4.387638|0.042814|13|12.37118|12.4355|74.67713
16|510310201011|5.625582|17.68377|9.38438|3.941244|0.021986|13|12.43731|12.51852|74.61279
17|510310209003|11.01746|15.09179|8.766409|1.896223|2.591414|12.03888|10.92236|11.55556|73.88008
18|510310205001|4.556935|17.73551|9.661037|0.999618|0.001157|12.78383|12.63066|12.70115|71.06989
19|510310204034|4.32369|17.54018|9.081469|3.300267|0.023914|13|11.45487|12.20307|70.92745
20|510310205003|4.751505|17.14568|8.570477|3.693247|0.03915|13|11.62273|11.95402|70.77682

## Appendices 
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/AreaWaterDensity.png">
</p>
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/BuildingDensity.png">
</p>
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/PreferredLand.png">
</p>
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/LinearWaterDensity.png">
</p>
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/ExistingParks.png">
</p>
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/PopulationDensity.png">
</p>
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/RoadsDensity.png">
</p>
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/CampbellCounty_NewRecreationalFacility/SlopeMean.png">
</p>
