## Introduction
In 2016, Hurricane Matthew tore through the Southern United States, including Virginia, Georgia, North and South Carolina. Specifically, Haw Watershed in North Carolina is at risk of flash flooding should another hurricane blow by. This flash flood model of Hurricane Matthew shows that the Haw Watershed is adversely affected by its urban cityscape, particular steep terrain and varied elevation, fine grained soil, and increased precipitation. All of these factors in addition to rain accumulation leads to a risk of flash flooding.
## Study Area 
Haw Watershed is located in the piedmont province in the north-central part of North Carolina, and is comprised of nine counties: Alamance County, Caswell County, Chatham County, Forsyth County, Guilford County, Orange County, Randolph County, Rockingham County, and Wake County. Figure 1 on the following page shows the outline of Haw Watershed, with the major roads and urban areas, along with lakes, ponds, streams, and rivers. The information depicted below will be helpful when comparing the different leveled flood risk areas further into our analysis. This watershed has varying elevation as shown in Figure 5, where the north-western areas appear to have higher elevation when compared to the eastern-central areas. 
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/HawWatershed_FlashFloodingAreas/HawMap.png">
</p> 
<p align = "center"> Figure 1.

## Methods 
Several factors were taken into account in order to determine the flood risk areas in the Haw Watershed. One is Land cover: the factor that affects flooding by influencing the amount of runoff during rainfall. Urbanized areas are more likely to experience flash flooding given the fact that more land is covered with cement and pavement, limiting soil absorption and increasing water buildup, or flooding. Soil, is the next factor that affects flooding, much like land cover, by influencing the amount of runoff water that is absorbed into soil. Areas with fine grained soils and clay are more likely to experience flash flooding since they have allowed less water through. Terrain, or elevation, is the factor that influences the amount of runoff water that accumulates on the surface, or into already existing bodies of water. Areas with steep terrain are more likely to experience flash flooding because water travels downward from the place where it falls. Precipitation, the final factor that affects flooding by being the source of the water that causes flooding. Areas with high precipitation are more likely to experience flash flooding. As seen in Figure 2 below, the central area of Haw Watershed received moderate to heavy rainfall, while the more northern areas received moderate to low rainfall during Hurricane Matthew in 2016. 
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/HawWatershed_FlashFloodingAreas/MattrRainfallAcc.png">
</p> 
<p align = "center"> Figure 2.
 
The soil and land cover datasets were combined based on their hydrologic groups. In order to combine the datasets, the soil data hydrologic groups had to be reclassified from “A”, “B”, “C”, and “D” to 1, 2, 3, and 4. The “A” group became 1, “B” became 2, “C” became 3, and “D” became 4. Following the combination of the datasets, the provided hydrologic soil curve value were applied using the reclassify tool. The soil retention layer was computed after the curve values were applied using the raster calculator and the provided equation: S = (1000.0 / CN) – 10.0, S means the soil retention prior to runoff, and CN stands for the curve number. Next, a runoff layer was calculated separately for the one-year storm data and the Hurricane Matthew data using the soil retention layer that was just created. The provided runoff equation: Q = (P-0.2S)^2 / (P+0.8S), Q meaning the amount of runoff, and P meaning the rainfall total for a given storm, along with the conditional function: Con, was used to calculate the runoff layers. 
Using the provided elevation data, the flow direction of the Haw Watershed was calculated by the flow direction tool. The flow accumulation for both the Hurricane Matthew data and one-year storm data was then calculated by using the flow direction and the runoff layer that was created right before. The raster calculator was then used to reclassify both flow accumulations by reclassifying the accumulations that were below 1000 to 0. The percentage of the one-year flow accumulation at all locations was then calculated by dividing the newly reclassified Hurricane Matthew flow accumulation by the one-year flow accumulation. The flash flood risk areas were then determined and are depicted in Figure 3 below. 
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/HawWatershed_FlashFloodingAreas/FloodRisk.png">
</p> 
<p align = "center"> Figure 3.

## Results
As seen in Figure 3 above, the south-eastern part of the Haw Watershed has moderate to very high probability while the north-western part has no to low probability of flash floods. For the most part, the urban areas have little to no probability of flooding. The final results in Figure 3, line up to the amount of precipitation depicted in Figure 2. The areas with high elevation as shown in Figure 5, seem to reside in the north-western part of the watershed and have little to no probability of flooding, while the areas with low to flat elevation appear to be the areas of high probability. Areas with high soil retention, like depicted in Figure 6, also appear to be in the areas of high elevation, and low probability of flash floods. The high soil retention areas are comprised of more granular soil, and forests so more water can be absorbed into the earth. The flow chart (Figure 4.) below outlines the methods of how the final results were determined.
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/HawWatershed_FlashFloodingAreas/HawFlowChart.png">
</p> 
<p align = "center"> Figure 4.
 
## Appendix
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/HawWatershed_FlashFloodingAreas/HawElevation.png">
</p> 
<p align = "center"> Figure 5.
<p align = "center">
<img width = "500" height = "350" src ="https://github.com/fernandezgk/GISPortfolio/blob/main/HawWatershed_FlashFloodingAreas/HawSoilRetention.png">
</p> 
<p align = "center"> Figure 6.
