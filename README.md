# 1000 Day Covid Analysis
Long-term measurements of our dynamic planet have been supplied by NASA's Earth Observing System Data and Information System (EOSDIS). The International Space Station, satellites, airborne campaigns, field campaigns, in situ equipment, and model outputs all contribute to the thousands of distinct data items in the EOSDIS collection.<br><br>

The Earth Observing System (EOS) is made up of a number of Earth sensing satellites, a science component, and a data system called the Earth Observing System Data and Information System, all of which are operated by NASA (EOSDIS). More than 2,400 Earth system science data products and associated services are distributed by NASA's Distributed Active Archive Centers (DAACs) for interdisciplinary investigations. These DAACs process, archive, document, and disseminate data from NASA's Earth system science research satellites and field projects from the past and present.<br><br>

Each centre supports one or more Earth science disciplines and delivers data products, data information, services, and tools that are unique to that science's user community. The Earth Science disciplines include Atmosphere, Calibrated Radiance and Solar Radiance, Cyrosphere, Human Dimensions, Land and Ocean.<br><br>

**The effects of Covid-19 on nitrogen dioxide and ozone air pollutants, surface temperature, night lights, snow cover, vegetation, and water level are examined in this study.**<br><br>

## SUMMARY
### Visualization for change in NO2 due to lockdown.<br>
![change in NO2 due to lockdown](https://github.com/Varchita-Beena/1000-Day-Covid-Analysis/blob/main/Omino2/analysis/no2_lockdown_change_visualisation.jpeg)

### Data Downloading
Data Name         | Download Size | Granules/Files| Format          | Extention | Library to read | Area| Downloaded Resolution and Gap | Resolution made and gap | 
------------------|---------------|---------------|-----------------|-----------|-----------------|-----|-------------------------------|-------------------------|
AIRS              | 54 GB         | 123           | HDF-EOS2 (hdf4) | .hdf      | pyhdf           |World| 1 degree, 8-day               | 1 degree, 8-day
Snow Cover        | 543 MB        | 127           | HDF-EOS2 (hdf4) | .hdf      | pyhdf           |World| 0.05 degree, 8-day            | 0.05, 0.025, 1 degree, 8-day
Lakes             | 189 MB        | -             | -               | .csv      | -               |World| -                             | -
Vegetation        | 6.5 GB        | 64            | HDF-EOS2  (hdf4)| .hdf      | pyhdf           |World| 0.05 degree, 16-day           | 0.05, 0.25, 1 degree, 16-day
Night Time Lights | 53 GB         | 14k           | HDF-EOS2 (hdf5) | .hdf5     | h5py            |India| 500 m, daily                  | 0.05, 0.25, 1 degree, daily and 8-day
Nitrogen Dioxide  | 12.51 GB      | 1004          | HDF-EOS2 (hdf5) | .hdf5     | h5py            |World| 0.25 degree, daily            | 0.05, 0.25, 1 degree for daily and 0.25, 1 degree for 8-day 

**Other two data sets of Cities having information about latitude, longitude, elevation etc of cities and CovidOxford having information about deaths, stringency index etc are also downloaded**

### Data Downloading Process<br>
After applying required filters (such as dates, Level 3, attributes etc), will get the script containing names of all the files/granules to be downloaded. Example AIRS data had 123 files, Night time lights had 14k files.<br>
Things to be taken care of while downloading data: <br>
1. Links from script file can be taken and can be downloaded one by one manually or if interface provides clickable links then those can also be useful.<br>
2. If all the files are to downloaded using script, then internet connection should be strong or if in the middle of the process something goes wrong then carefully look at the files downloaded and edit accordingly in the script.<br>
3. If there are a lot of files or too large files then the downloading process will be very slow. Parallelization can be used to increase the effiency of downloading. Prepare number of different scripts with different file names and execute them parallely. (most helpful for Night Time Light)

### Summary of the way analysis is done.<br>
1. Weekwise metric average of all cities of 2019 and 2020<br>
2. Difference in metric values between the same week of 2020 and 2019<br>
3. Pre and Post lockdown in 2020<br>
4. Comparison of percentage change between pre and post lockdown dates of 2019 and 2020<br>
5. Impact of covid-19 on metric compared to pre-lockdown dates' values (Regression)<br>
6. For fe metric (vegetation index, snow cover) analysis is done across the globe<br>
7. Dimensionality reduction is applied on 20 metrics (metrics from all datasets are taken).
8. How much metric values are correlated with covid stringency_index (how strict the lockdown was),retail_and_recreation, residential, new_cases_smoothed_per_million.

### Summary of the results<br>
(Few points are shown here. Detail analysis can be found in the analysis directory of every dataset)<br>
1. If controlled for pre-lockdown (march first-week) values, covid leads to increase in O3 values. Covid leads to decrease in O3 after lockdown compared to pre-lockdown values<br>
2. Surface Skin Temperature(at night) decreased due to covid by 1.86 degrees at night between first week of march and first week of april (second week of lockdown). Covid leads to decrease in Surface skin temperature (at day) of 1.5 to 2 degrees<br>
3. Reducing the dimensionality from 20 to 1 (20 metrics were taken). In total 39% variance is explained by the component. The max is captured for metric CloudFrc_TqJ_A, RelHumSurf_TqJ_A etc. Even good amount of varaince from surface skin temperature, NDVI (vegetation index), EVI (vegetation index) etc is also captured.<br>
4. Over all not much change in water level.<br>
5. In 2020 clear reduction of night time lights for navratri festivalis seen for cities of Gujarat (Ahmedabad, Nadiad, Vadodara, Surat, Rajkot). For both 2019 and 2020, from April, there is clear decline in night time lights. But for 2020, it is clearly higher compared to 2019. Towards the end of the year, the values for 2020 rise up again and become close to their 2019 counter parts.<br>
6. Bangalore and Lucknow observed around 16% decrease in NO2 in second week of lockdown compared to first week of march. Cities with more than 1 million population observed around 3.5 decrease. In the lockdown period, in 2020 the NO2 levels decreased by 10% compared to pre-pandemic levels compared to 1-2% increase in 2019. From regression analysis, the negative coefficient of covid indicator variable shows that in the covid-year the NO2 levels declined during lockdowns compared to pre-lockdown levels. As the lockdown progresses, the dip even got bigger and increased by 3-4 times. Clearly, covid-19 related lockdowns lead to reduction in NO2 levels. The correlations of daily NO2 levels for indian cities with covid oxford data are good for first wave and very weak for second wave<br>
7. The snow cover hasnt actually increased in 2020. So probably, the melting of snow is dynamic and is different in amount in different weeks. It looks like in lockdown months the decrease in snow cover is lesser in 2020 compared to 2019, but the snow cover in total hasnt changed much. The same case is for snow cover across the globe. Regression does show probable increase of snow cover of 3 points during middle months of 2020 compared to 2019. However, it is very tough to conclude anything from this.<br>
8. Overall not much change in vegetation index<br><br>


### Future work and some points
1. Using PCA (dimensionality reduction) we have got a component say Environment Index for now. Next we have to transform every data point to this component and then do the analysis of this component as descibed in other analysis notebooks. It will an analysis of combination of features/metrics.<br>
2. To understand properly the change in the different domains, little expert/domain knowledge is also needed. We say there ie not significant change in Vegetation index, that can be due to rainfall in last years. Next it is very import to understand how a that domain works. Vegetation is not related to one metrics or few metrics. Seasons should also be taken in the account for analysis. May be the month on which analysis is done can have reduced pollution but may have man induced fires for maintaining the fields.<br>
3. Our main question is: Is there any change in environment due to covid-19. To explore this apart from all the things described above, clustering can also be done to find answer about this. It is possible that we can get multimodel distributions in clusters for covid and non-covid year. How are those distributions for non covid year v/s for covid time. Distributions regarding change in metrics during lockdown periods can also be seen in clusters.<br>
4. Above is in terms of covid and non covid. Another is how cities have responded during covid. This analysis can give us groups stating the ways cities have responded. Here groups imply clusters.<br>
5. Clusters regarding different waves can also be analysed. 

## Is this really necessary?<br>
Enormous effects are in place to restore the environment standards. But in the last few months, the coronavirus lockdown has led to a drop in pollution across the world. The contingency measure has improved air and water quality, clean beaches and environmental noise reduction.<br> As companies, transportation, and campaigns have stopped down, there has been a noticeable drop in GreenHouse Gases (GHGs) emissions. Because automobiles and people were both inside the dwellings, air pollution had lessened. The shutdown of heavy industries resulted in a reduction in N2O and CO emissions, as well as a reduction in NO2 emissions from fossil fuel combustion in several countries (e.g., US, Canada, China, India, Italy, Brazil, etc.) It is the most important indicator of global economic activity. Acid rain is primarily created by the interaction of NO2 and water.<br><br>

Several respiratory disorders are caused by O2 and H2O. However, due to the epidemic, all of these have been reduced. Numerous international flights have been cancelled in many countries throughout the world because of restrictions on international travellers' ability to enter and exit. Because of the statewide lockdown, air traffic fell globally compared to the same period last year, having a significant impact on the environment. It is an immense aid to withstand global climate change for the reduced consumption of fossil fuels. In nations like India and Bangladesh, where industrial and residential wastes are dumped into rivers with no method, water pollution is a typical calamity. During the epidemic, however, it was halted or decreased since many industries were shut down.<br><br>

On the other side, there were also detrimental environmental implications. Medical waste creation soared internationally during the Covid-19 outbreak, posing a concern to public health and the environment.<br><br>

The natural ecosystems and various flora and animals are in grave danger because of the various countries' lockdowns. Various protected areas, such as natural parks, marine conservation zones, and wildlife sanctuaries, were left under surveillance since two persons who worked in such regions were stranded at home. It exacerbated problems such as wildlife poaching, illicit deforestation, and fishing. Because ecotourism is seen as a major source of cash, the abrupt shutdown of ecotourism activities in tourist destinations and forest regions has increased unemployment. The stalemate has had an influence on the environment, the economy, tourism, and personal health. It has infiltrated every element of human and environmental life. Environmental communication is critical, as we can see. Mostly it entails human interaction with nature. We recognise that COVID-19 serves as a reminder of the human-environment relationship. To avoid future outbreaks, we must address ecological and wildlife risks like habitat loss, illegal trade, pollution, and climate change.<br><br>
 
More details about whay this is necessary can be found in the [Times of India article](https://timesofindia.indiatimes.com/readersblog/world-of-words/covid-19-and-its-impact-on-environment-34088/)
