One of the key goals of the Earth Observing System (EOS) programme is to understand how the Earth functions as a system by studying the quantity and role of terrestrial vegetation in large-scale global processes. This necessitates knowledge of the global distribution of vegetation types, as well as their biophysical and structural qualities, as well as their spatial and temporal fluctuations. The Vegetation Indices (VI) are reliable empirical indicators of vegetation activity at the surface of the earth. They are designed to enhance the vegetation reflected signal from measured spectral
responses by combining two (or more) wavebands, often in the red (0.6 - 0.7 μm) and NIR wavelengths (0.7-1.1 μm) regions.<br><br>

# The MODIS vegetation index (VI) products
Two VI products are made globally for land regions. The first product is the standard Normalized Difference Vegetation Index (NDVI). The second VI product is the Enhanced Vegetation Index (EVI).
<br><br>
The theoretical basis for empirical-based vegetation indices is derived from examination of typical spectral reflectance signatures of leaves. Examining typical spectral reflectance characteristics of leaves provides the theoretical foundation for empirically-based vegetation indicators. Because of strong absorption by photosynthetically active pigments, reflected energy in the visible is very low, with maximum absorption values in the blue (470 nm) and red (670 nm) wavelengths. Nearly all near-infrared radiation (NIR) is scattered (reflected and transmitted) back with very little absorption, in a way that is determined by the canopy's structural qualities (LAI, leaf angle distribution, leaf morphology).<br><br>
As a result, the difference between red and near-infrared responses (also known as the red shift) is a sensitive indicator of vegetation abundance, with maximal redNIR differences happening over a complete canopy and minimal contrast occurring over targets with little or no vegetation. The contrast is a result of both red and NIR changes for low and medium amounts of vegetation, but when the red band gets saturated owing to chlorophyll absorption, only the NIR contributes to increased contrasts for higher amounts of vegetation.<br><br>
## NDVI
The NDVI is a normalized transform of the NIR to red reflectance ratio. It is commonly expressed as: <br>
**NDVI** = NIR - Red / NIR + Red

## EVI
To minimizing atmospheric effect the difference in blue and red reflectances can be used as an estimator of the atmosphere influence level. This concept is based on the wavelength dependency of aerosol scattering cross sections. In general the scattering cross section in the blue band is larger than that in
the red band. When the aerosol concentration is higher, the difference in the two bands becomes larger. This information is used to stabilize the index value against variations in aerosol concentration levels.The EVI formula is written as:<br>
**EVI** = G(NIR - Red / NIR +C1Red - C2Blue  + L)<br>
G - Scaling factor<br>
L is the canopy background adjustment<br>
NIR, Red, and Blue are the full or partially atmospheric surface reflectances

