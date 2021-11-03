**NO2 is one of the major air pollutants.**
## Dataset
* The OMI Level-3 data product contains averaged NO2 vertical columns, reported on a 0.250 x 0.250 geographical grid.<br>
* The following is an example of a file name: OMI-Aura_L3-OMNO2d_2004m1024_v003-2013m0109t111834.he5<br>
* Instrument ID_DataType_Data ID_Version.Suffix<br>
* Instrument ID -> OMI-Aura, Data Type -> L3-OMNO2d, DATA ID -> <date> (<yyyy>m<mmdd>), Version -> v<version>-<production date and time>, Suffix -> he5<br>
* The format of the data file is HDF-EOS 5<br>
  
**Every thing related to week mappings and preparaing data at any degree is explained AIRS and Vegetation directories.**<br><br>
 
## Analysis
Few points:<br>
* Bangalore and Lucknow observed around 16% decrease in NO2 in second week of lockdown compared to first week of march. Cities with more than 1 million population observed around 3.5 decrease.<br>
* Regression tells us: *The negative coefficient of covid indicator variable shows that in the covid-year the NO2 levels declined during lockdowns compared to pre-lockdown levels. As the lockdown progresses, the dip even got bigger and increased by 3-4 times. Clearly, covid-19 related lockdowns lead to reduction in NO2 levels.*<br>
* The correlations of daily NO2 levels for indian cities with covid oxford data are good for first wave and very weak for second wave<br>
**Detailed analysis can be found in anaysis directory**<br><br>
## Referred paper.
[COVID-19 IMPACT ON ASIAN EMISSIONS: INSIGHT FROM SPACE OBSERVATIONS](https://www2.acom.ucar.edu/news/covid-19-impact-asian-emissions-insight-space-observations?_ga=2.94930140.194184266.1635963992-335902505.1634714874)<br>
This study shows us: The changes in tropospheric carbon monoxide (CO) over eastern China using NASA Terra/MOPITT and ESA S5P/TROPOMI data. The changes between the early lockdown period (1 February to 10 March 2020) and the equivalent period in the 2019 season are consistently quantified by the two datasets. They find approximately 30 to 45% peak reductions in CO comparing the post Chinese New Year (CNY) periods in 2020 to 2019. Their results indicate that CO in the Beijing-Chengdu-Shanghai-Wuhan area has decreased on average by almost 6%, with more than 46% reduction locally. CO increase over SE Asia is consistent with seasonal fires, also observed by the MODIS instruments. Their study period is Chinese New Year of 2019 (4-10 feb) and 2020 (24 - 30 jan)<br><br>
 The much wider extent and magnitude of the decrease in NO2 compared to CO reflects the different sources and lifetimes of the two pollutants. CO lifetime is a few months in winter, so measurements include contributions from globally transported CO. NO2 lifetime is hours to days, so observations show local emission sources much more directly than CO. There are also differences in emission sources for CO and NO2. We would expect the industry and transportation sectors to be most affected by the lockdown and both have CO and NO2 emissions. However, the largest source of CO in Asia is the residential sector, which would likely not have reductions due to the lockdown.<br><br>

  
