###About the CSV's in this directory:

The `zoning_codes_fix*` csv's in this directory are a remnant of fixing up the legacy zoning codes data and should eventually just be folded into the zoning_lookup.csv in the bayarea_urbansim repository.

`zoning_source_metadata.csv` is the key descriptor of the metadata that we have about zoning and general plan data that was collected as part of the 2012 collection effort.

The shapefiles listed in zoning_source_metadata.csv are used directly in the Makefile in order to fetch and then load all zoning and general plan from the 2012 effort.

`zoning_table_city_lookup.csv` is meant to be a list of all jurisdictions in the Bay Area. It is used to look up jurisdiction common names, and which jurisdictions are to be assigned zoning and general plan data from the 2006 data collection effort. In the future, we can probably just fold these 2 csv's together, at least in the database table representing all the jurisdictions.

###About data used generally in this repository:

As for other data used here, the following are required (and accessible with the Makefile in the root directory)

filename|description
---------------|--------------
jurisdictional/*.shp | A directory of shapefiles of Zoning and General plans for the jurisdictions in the Bay Area--details in zoning_source_metadata.csv
a parcel table | these are assembled from source data [with this script](https://github.com/MetropolitanTransportationCommission/bayarea_urbansim/blob/master/data_regeneration/run.py)
city10_ba.shp | city boundaries (2010 census) MTC edits for water-features and others
county10_ca.shp | county boundaries (2010 census) MTC edits for water-features and others
zoning_codes_base2012.csv | Use these to map specific jurisdictional zoning to a generic taxonomy-from this [table](http://landuse.s3.amazonaws.com/zoning/zoning_codes_base2012.csv)
match_fields_tables_zoning_2012_source.csv | Names the column used in Zoning V2 which is used in the zoning taxonomy - from the [Project Management Spreadsheet](http://landuse.s3.amazonaws.com/zoning/CityAssignments_Nov3_2014.xlsx)
plu06_may2015estimate.shp | PLU 2006 data from [ABAG](http://gis.abag.ca.gov/)

