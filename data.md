### NAIP

Using this page:

https://datagateway.nrcs.usda.gov/GDGHome_DirectDownLoad.aspx

We can find link to: National Ag. Imagery Program County Mosaic

Has years: 2004-2018

Reference files (2): NAIP File Name.pdf and Degree blocks by State.xlsx

Each state listed may have a few extraneous files, such as imagery or a note.

Each state listed may have _c and _n imagery (unsure of difference).

Each imagery zip file is for one part of the state.

Each zip file contains one .sid image(?) file.

There is a 15 gb download limit (daily? hourly? per download? per IP?) on box.com.

MrSID is a compression scheme created by LizardTech. More information on MrSID is available via LizardTech paper or Wikipedia:

https://doc.lizardtech.com/files/mrsid/MrSID_White_Paper.pdf

https://en.wikipedia.org/wiki/MrSID

Instructions for converting .sid to .tiff are available at:

http://www.paulnorman.ca/blog/2011/03/converting-mrsid-to-geotiff/

1. Download MrSID SDK.
2. Ensure that GDAL is installed on the system (occasionally included de facto in Linux).
3. Convert to .tif:

> $ ./mrsiddecode -wf -i /home/dave/Downloads/ortho_1-1_hc_s_nm028_2018_1/ortho_1-1_hc_s_nm028_2018_1.sid -o test.tif

For example, this converts a compressed .sid file (170 MB) into an uncompressed .tif file (6.8 GB).

We now have a GeoTiff* file that may be used with geo-polygons to train a CNN. For example, here: (https://github.com/PlatformStories/train-cnn-classifier).

\* Ritter, N., Ruth, M., Grissom, B. B., Galang, G., Haller, J., Stephenson, G., ... & Messina, J. (2000). Geotiff format specification geotiff revision 1.0. SPOT Image Corp.

### GRanD dataset (Reservoir and Dam Polygons)

Dataset is available here:

http://globaldamwatch.org/data/#core_global

Latest version is 1.3 (2019).

Dataset shape files:

1. Reservoirs: GRanD_reservoirs_v1_3.shp (65 MB)
2. Dams: GRanD_dams_v1_3.shp (205 KB)

Dataset documentation: GRanD_Technical_Documentation_v1_3.pdf






