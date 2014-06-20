#**Processing MODIS data**

The application provides data processing from MODIS satellite missions. Input data is
always folder with more then one raster. Communication with external programs
(GDAL, SAGA) is realized using a thread with Java (JavaFX) programming language.

Application is made for desktop and using next technologies:

1. _JavaFX (program is written in EclipseFX)_

2. _GDAL library ([GDAL](http://www.gdal.org/))_

3. _SAGA GIS ([SAGA](http://www.saga-gis.org/en/index.html))_

4. _iText, Programmable PDF Software ([iText](http://itextpdf.com/))_

Application is divided in two parts, one is code in Java programming language and second is style for application in Cascading Style Sheets (CSS). 

Code does not have a lot of comments. 

Application have 4 main parts, 4 operations:

- ###format changes

> Changing the format using GDAL from .hdf to .gtiff – result are three channels,
and then using SAGA (System for Automated Geoscientific Analyses) changing
format to .sgrd.

- ###masking

> Cutting raster into selected area - only the first two channels, using SAGA.

- ###NDVI

> In the end, application calculate NDVI (Normalized Difference Vegetation Index)
from the first two channels.

- ###save process to pdf

> Any part of the process can be saved in .pdf format - stores date / time of
processing, first and last name of raster, applied operations, the number of rasters
and written notes. On this way it's always possible to check rasters that are
processed and store notes (for example, which rasters need to be processed).

