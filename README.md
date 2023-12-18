# Classification of galaxy and NSC
Welcome here. We provide here the HR-CelestialNet code (PyTorch), the list of LCID test sets, and the list of Blurry verification sets from the project exploring galaxies and NSC classification.
## HR-CelestialNet.py
Contained here is the core CNN network of HR-CelestialNet, designed for galaxy and NSC classification using PyTorch. For training purposes, you may need to add specific parameters in the training process, such as the optimizer, learning rate, and others.
## LCID_test.csv and blurry_validation.csv
To optimize memory usage, we have enriched the dataset table with various fields, including ID, Instrument, OBSID, Filter, RA, DEC, HDU_Index, and Label. These fields provide essential information about each observation instead of directly storing the image data. Here's how you can retrieve the images:
- Copy the OBSID, and search in [MAST](https://mast.stsci.edu/portal/Mashup/Clients/Mast/Portal.html) (click "Search by OBSID");
- Dowload FITS files,  We experiment with files with the **raw.fits** suffix;
- Read files,  **HDU_Index** indicates the position of this image within the FITS file，you need to follow it to read the image accurately.

### If you use the code or dataset provided in this repository in your research, please cite the following [paper](https://academic.oup.com/mnras/advance-article/doi/10.1093/mnras/stad3815/7476003):

@article{10.1093/mnras/stad3815,
    author = {Zhang, Yuquan and Cao, Zhong and Wang, Feng and Lam, Man I and Deng, Hui and Mei, Ying and Tan, Lei},
    title = "{Scientific Preparation for CSST: Classification of galaxy and Nebula/Star Cluster based on deep learning}",
    journal = {Monthly Notices of the Royal Astronomical Society},
    pages = {stad3815},
    year = {2023},
    month = {12},
    issn = {0035-8711},
    doi = {10.1093/mnras/stad3815},
    url = {https://doi.org/10.1093/mnras/stad3815}}

Thank you for citing our work.
