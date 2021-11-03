* We are trying to make 1 component from all the metrics.<br>
* We are reducing the dimensionality from 20 to 1. <br>
* The percentage of variance explained by each of the selected components is given by explained_varianceratio. <br>
* Here in total 39% variance is explained by the component. <br>
* The max is captured for metric CloudFrc_TqJ_A, RelHumSurf_TqJ_A etc. Even good amount of varaince from surface skin temperature, NDVI, EVI etc is also captured.<br>
* All 20 metrics: SurfSkinTemp_TqJ_A, SurfAirTemp_TqJ_A, TropPres_TqJ_A, TropTemp_TqJ_A, TotH2OVap_TqJ_A, H2O_MMR_Surf_TqJ_A, RelHumSurf_TqJ_A, RelHumSurf_liquid_TqJ_A, TropHeight_TqJ_A, CloudFrc_TqJ_A, CloudTopPres_TqJ_A, CloudTopTemp_TqJ_A, TotO3_TqJ_A, OLR_TqJ_A, CMG 0.05 Deg 16 days NDVI, CMG 0.05 Deg 16 days EVI, Eight_Day_CMG_Snow_Cover, Gap_Filled_DNB_BRDF-Corrected_NTL, ColumnAmountNO2, ColumnAmountNO2Trop.<br>
* These all 20 metrics are from Night time lights, Nitrogen dioxide, Vegetation index, Snow cover, Ozone.
* Future work: Next we have to transform every data point to this component and then do the analysis of this component as descibed in other analysis notebooks. The difference is all those are done in isolation, here the information from all metrics are taken. We can see how this component is behvaing in 2019 vs in 2020 or in pre and post period of covid-19 etc.
