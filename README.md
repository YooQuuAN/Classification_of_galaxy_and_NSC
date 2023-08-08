# Classification_of_galaxy_and_NSC
Welcome here. We provide here the HR-CelestialNet code (Pytorch), the list of LCID test sets, and the list of Blurry verification sets from the project exploring galaxies and NSC classification.
## HR-CelestialNet.py
Contained here is the core CNN network of HR-CelestialNet, designed for galaxy and NSC classification using PyTorch. For training purposes, you may need to add specific parameters in the training process, such as the optimizer, learning rate, and others.
## LCID_test.csv and blurry_validation.csv
To optimize memory usage, we have enriched the dataset table with various fields, including ID, Instrument, OBSID, Filter, RA, DEC, HDU_Index, and Label. These fields provide essential information about each observation instead of directly storing the image data. Here's how you can retrieve the images:
- Copy the OBSID, and search in [MAST](https://mast.stsci.edu/portal/Mashup/Clients/Mast/Portal.html) (click "Search by OBSID").
- Dowload FITS files,  We experiment with files with the raw.fits suffix.
- Read files ,  **HDU_Index** indicates the position of this image within the FITS file，You need to follow it to read the image accurately.
