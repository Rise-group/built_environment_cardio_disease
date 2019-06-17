# Code

## Structure

Python and R notebooks used for specific data processing tasks:

### 0_Mortality_rates_maps:
Load mortality rates from MS Excel file as sent by Silvana Zapata from the Medellin's Health Secretary, load administrative neighborhoods downloaded from Medellin's OpenData portal, match both and produce mortality maps by neighborhood for different diseases (counts, raw rates and adjusted rates).

### 1_ODSurvey2017_zones_selection_v2:
Selection of OD zones that are urban and main destinations of trips from urban areas. Data: Encuesta Origen y Destino 2017, Área Metropolitana del Valle de Aburrá (EOD_2017_sintesis.xlsx). Data source: Juan Pablo Ospina, PhD(c) RiSE Group (May 2019). Goal: to select the SIT zones that are the destination from Medellin's urban SIT zones, weighted by the number of persons that made the trips (not by the number of trips because one person usually records more than one trip in the OD Survey). 

### 2_landsat_download:
Google Earth Engine bulk download of surface reflectance (with atmospheric correction) Landsat images and clipped to the area of interest (roi). Images selected previously using Earth Explorer and visual assessment: cloud cover less than 30% over land. The images are stored in the users Google Drive folder.

### 3_Free cloud landsat composite:
R notebook with the process to mask clouds and shadows on a Landsat 8 image series, perform radiometric normalization and fill those areas of the selected reference image with cloud-free pixels from previous Landsat images. Normalized difference indexes are computed and written to disk at the end: NDVI, NDWI, and NDBI.

### 4_zonal_stats_by_SITzones_and_neighborhoods:
Extraction of zonal stats from images (or raster datasets) for Medellin Administrative neighborhoods and Origin-Destination areas (SIT zones).

### 5_sit2neigh:
Redistribution of Origin-Destination flows (from OD 2017 Survey) to administrative neighborhoods, weighted by area share.

### 6_OSMnx metrics:
Extraction of selected street network metrics by neighborhood or SIT zone using the OSMnx library (Boeing, 2017). The selected metrics for this work are: circuity_avg (circuity), street_density_km, int_dens_km (intersection density), k_avg (average node degree of the graph within the polygon).

## Setup

If necessary


