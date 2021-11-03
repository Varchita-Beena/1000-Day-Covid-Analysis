LakePy is the pythonic user-centered front-end to the [Global Lake Level Database](https://github.com/ESIPFed/Global-Lake-Level-Database). This package can instantly deliver lake water levels for some 2000+ lakes scattered across the globe. <br>
The Global Lake Level Database (GLLD) is the back-end architecture for the Python package LakePy. The GLLD hosts historic lake level data on an Amazon Web Services (AWS) Relational Database Service (RDS).Currently the GLLD data comes from three sources (so far!)<br>

[United States Geological Survey National Water Information System](https://waterdata.usgs.gov/nwis)<br>
[United States Department of Agriculture: Foriegn Agricultural Service's G-REALM Database](https://ipad.fas.usda.gov/cropexplorer/global_reservoir/)<br>
[Theia's HydroWeb Database](http://hydroweb.theia-land.fr/)<br><br>

The GLLD consists of two tables:<br>
reference_ID<br>
lake_water_level<br><br>
The reference_ID table contains the Unique ID Number, Lake Name, Original Source, and Metadata, of all lakes. The Unique ID Number is assigned incrementally as new lakes are added to the GLLD. This is the primary key for the MySQL table. This number is what is primarly used to identify and reference lakes in the GLLD and LakePy. If the same lake exists from multiple sources, there will be two lakes with a unique ID. For example, Lake Mead exists in both the hydroweb data and the USGS data. <br>
|id_No	| source	  | lake_name|
|-------|-----------|----------|
|138	  | hydroweb	| Mead      |
|1556	  | usgs	    | MEAD LAKE WEST BAY NEAR WILLARD, WI|

The lake name is copied exactly as is from the original data source. The source identifies which of the three original data sources the data comes from. Finally the metadata stores all available metadata from the data source as a JSON array.<br>

The lake_water_level table contains the actual historic data for each lake. This table uses a composite primary key of the Unique ID Number and date (YYYY-MM-DD) for the MYSQL table. This method of a composite primary key limits the GLLD to have a maximum resolution of one unique lake measurement per day for each lake.<br>
In general this data is not very consistent. It has a lot of missing values. It does not have standard format to use.

