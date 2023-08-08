# Classification_of_galaxy_and_NSC
Welcome here. We provide here the HR-CelestialNet code (Pytorch), the list of LCID test sets, and the list of Blurry verification sets from the project exploring galaxies and NSC classification.
## HR-CelestialNet.py
Only the CNN network itself is included here. If training is required, parameters in the training process, such as optimizer, learning rate and so on, need to be added by themselves.
## LCID_test.csv and blurry_validation.csv
We added a lot of fields like ID, Instrument,OBSID, Filter, RA, DEC, HDU_Index,Label to the dataset table instead of the direct image data. This is because large images take up a lot of memory. Here is how to get the image from the table:
- Copy the OBSID, and search in [MAST](https://mast.stsci.edu/portal/Mashup/Clients/Mast/Portal.html) (click "Search by OBSID")
- Dowload FITS files,  We experiment with files with the raw.fits suffix.
- Read files ,  **HDU_Index** indicates the position of this image within the FITS file，You need to follow it to read the image accurately.
