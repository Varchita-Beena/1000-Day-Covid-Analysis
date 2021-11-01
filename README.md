# 1000 Day Covid Analysis
Long-term measurements of our dynamic planet have been supplied by NASA's Earth Observing System Data and Information System (EOSDIS). The International Space Station, satellites, airborne campaigns, field campaigns, in situ equipment, and model outputs all contribute to the thousands of distinct data items in the EOSDIS collection.<br><br>

The Earth Observing System (EOS) is made up of a number of Earth sensing satellites, a science component, and a data system called the Earth Observing System Data and Information System, all of which are operated by NASA (EOSDIS). More than 2,400 Earth system science data products and associated services are distributed by NASA's Distributed Active Archive Centers (DAACs) for interdisciplinary investigations. These DAACs process, archive, document, and disseminate data from NASA's Earth system science research satellites and field projects from the past and present.<br><br>

Each centre supports one or more Earth science disciplines and delivers data products, data information, services, and tools that are unique to that science's user community. The Earth Science disciplines include Atmosphere, Calibrated Radiance and Solar Radiance, Cyrosphere, Human Dimensions, Land and Ocean.<br><br>

**The effects of lockdown on nitrogen dioxide and ozone air pollutants, surface temperature, night lights, snow cover, vegetation, and water level are examined in this study.**<br><br>

## SUMMARY
### Data Downloading
Data Name         | Download Size | Granules/Files| Format          | Extention | Library to read | Area| Downloaded Resolution and Gap | Resolution made and gap | 
------------------|---------------|---------------|-----------------|-----------|-----------------|-----|-------------------------------|-------------------------|
AIRS              | 54 GB         | 123           | HDF-EOS2 (hdf4) | .hdf      | pyhdf           |World| 1 degree, 8-day               | 1 degree, 8-day
Snow Cover        | 543 MB        | 127           | HDF-EOS2 (hdf4) | .hdf      | pyhdf           |World| 0.05 degree, 16-day           | 0.05, 0.025, 1 degree, 16-day
Lakes             | 189 MB        | -             | -               | .csv      | -               |World| -                             | -
Vegetation        | 6.5 GB        | 64            | HDF-EOS2        | .hdf      | pyhdf           |World| 0.05 degree, 16-day           | 0.05, 0.25, 1 degree, 16-day
Night Time Lights | 53 GB         | 14k           | HDF5            | .hdf5     | h5py            |India| 500 m, daily                  | 0.05, 0.25, 1 degree, daily and 8-day
Nitrogen Dioxide  | 12.51 GB      | 1004          | HDF5            | .hdf5     | h5py            |World| 0.25 degree, daily            | 0.05, 0.25, 1 degree for daily and 0.25, 1 degree for 8-day 

### Data Downloading Process<br>
After applying required filters (such as dates, Level 3, attributes etc), will get the script containing names of all the files/granules to be downloaded. Example AIRS data had 123 files, Night time lights had 14k files.<br>
Things to be taken care of while downloading data: <br>
1. Links from script file can be taken and can be downloaded one by one manually or if interface provides clickable links then those can also be useful.<br>
2. If all the files are to downloaded using script, then internet connection should be strong or if in the middle of the process something goes wrong then carefully look at the files downloaded and edit accordingly in the script.<br>
3. If there are a lot of files or too large files then the downloading process will be very slow. Parallelization can be used to increase the effiency of downloading. Prepare number of different scripts with different file names and execute them parallely. (most helpful for Night Time Light)



##### Is this really necessary?<br>
Enormous effects are in place to restore the environment standards. But in the last few months, the coronavirus lockdown has led to a drop in pollution across the world. The contingency measure has improved air and water quality, clean beaches and environmental noise reduction.<br> As companies, transportation, and campaigns have stopped down, there has been a noticeable drop in GreenHouse Gases (GHGs) emissions. Because automobiles and people were both inside the dwellings, air pollution had lessened. The shutdown of heavy industries resulted in a reduction in N2O and CO emissions, as well as a reduction in NO2 emissions from fossil fuel combustion in several countries (e.g., US, Canada, China, India, Italy, Brazil, etc.) It is the most important indicator of global economic activity. Acid rain is primarily created by the interaction of NO2 and water.<br><br>

Several respiratory disorders are caused by O2 and H2O. However, due to the epidemic, all of these have been reduced. Numerous international flights have been cancelled in many countries throughout the world because of restrictions on international travellers' ability to enter and exit. Because of the statewide lockdown, air traffic fell globally compared to the same period last year, having a significant impact on the environment. It is an immense aid to withstand global climate change for the reduced consumption of fossil fuels. In nations like India and Bangladesh, where industrial and residential wastes are dumped into rivers with no method, water pollution is a typical calamity. During the epidemic, however, it was halted or decreased since many industries were shut down.<br><br>

On the other side, there were also detrimental environmental implications. Medical waste creation soared internationally during the Covid-19 outbreak, posing a concern to public health and the environment.<br><br>

The natural ecosystems and various flora and animals are in grave danger because of the various countries' lockdowns. Various protected areas, such as natural parks, marine conservation zones, and wildlife sanctuaries, were left under surveillance since two persons who worked in such regions were stranded at home. It exacerbated problems such as wildlife poaching, illicit deforestation, and fishing. Because ecotourism is seen as a major source of cash, the abrupt shutdown of ecotourism activities in tourist destinations and forest regions has increased unemployment. The stalemate has had an influence on the environment, the economy, tourism, and personal health. It has infiltrated every element of human and environmental life. Environmental communication is critical, as we can see. Mostly it entails human interaction with nature. We recognise that COVID-19 serves as a reminder of the human-environment relationship. To avoid future outbreaks, we must address ecological and wildlife risks like habitat loss, illegal trade, pollution, and climate change.<br><br>
 
More details can be found in the [Times of India article](https://timesofindia.indiatimes.com/readersblog/world-of-words/covid-19-and-its-impact-on-environment-34088/)
