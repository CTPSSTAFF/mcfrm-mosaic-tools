# MC-FRM LEVEL_1 data raster mosaic-ing tool

## Background
The raw LEVEL_l MC-FRM data is shipped in a highly 'fragmented' form:
a single TIF file for each municipality for each year (present=2018,
2030, 2050, 2070) and for each 'kind' of data (probability, 
depth at 0.1% probability, depth at 0.5% proabaility, depth at 1% probability).
Futher complicating matters, the TIF files for 'North' municipalities are 
stored a a separate folder for 'South' municipalities.

The following figure summarizes the organization of the data, as shipped:
```
LEVEL_1/
    Year/
      North-or-South/
          Kind-of-data/
              individual TIF files
```

## Purpose
The purpose of this tool is to create a single raster mosaic for 
each \{year, data\_kind\} pair from all the relevant TIFs.

## Inputs
Individual raster TIF files, one per town covered by the MC-FRM data, for each:
\{year, data_kind\} pair, where _year_ may be 'Present', '2030', '2050, or '2070',
and _data\_kind_ may be 'Probability', 'Depth_1_percent', 'Depth_0.5_percent' or
'Depth_0.1_percent'.

## Outputs
A single raster mosaic dataset in a File Geodatabase for each \{year, data_kind\} pair.

## Execution
This script is inteneded to be run in the interactive Python console
in ArcMap or ArcGIS Pro. Converting it into an ESRI "toolbox" tool 
is left as an exercise for the reader.

## Colophon
Author: Ben Krepp  
Date: 18 May 2023, 30 May 2023
