## Introduction

The main documentation for **Feature-Based Molecular Networking** [can be accessed here](docs/fbmn.md). See [our article](https://www.nature.com/articles/s41592-020-0933-6).

Below we describe how to use **Progenesis QI** with the FBMN workflow on [GNPS2](https://gnps2.org/homepage).

## Using Progenesis QI and the Feature-Based Molecular Networking on GNPS2

Progenesis QI is a proprietary LC-MS feature detection and alignment software developed by [Nonlinear Dynamics](http://www.nonlinear.com/progenesis/qi/) that is compatible with Waters file format and other proprietary and open mass spectrometry format.

Progenesis QI can perform feature detection, alignment and annotation of non-targeted LC-MS/MS data acquired either **in data-dependent analysis (DDA)** or **MSE data independent analysis (DIA)**, and can also uses the **ion mobility spectrometry (IMS) dimension**. Feature-based molecular networking (FBMN) can be performed on **any of these data types processed with Progenesis QI**.

## Running Progenesis QI for feature-based molecular networking on GNPS2

For more information on Progenesis QI, please refer to the official documentation at: [http://www.nonlinear.com/progenesis/qi/](http://www.nonlinear.com/progenesis/qi/).

##### 1. Import and process the mass spectrometry data with Progenesis QI
- In Progenesis QI (ver. 2.4, Nonlinear Dynamics), **import RAW data** from Waters QTof data-independent acquisition (DIA) modes such as SONAR, MSE or HDMSE. 
- **Processed data** with Progenesis QI and export the results for GNPS2 analysis as indicated below. See the [Progenesis QI LC-MS tutorial](http://www.nonlinear.com/products/progenesis/lc-ms/tutorial/) and the [tutorial videos](https://www.youtube.com/watch?v=hurottpvEO8&list=PLKkdMSX1HQ-UD8WVe9T9pcEWMzyw20FUi) for more informations.

##### 2. Export the processing results

In the menu, under the “Identify Compounds” tab:

- Select **“Export Compound Measurement”** to export the **feature quantification table** (CSV file) containing compound intensity and annotation can be exported (see below).
- Select **“Export fragment database”** to the export the **MS/MS spectral summary** (MSP file) containing the list of representative MS/MS spectra (see below). **NOTE: Do not select tags to export**

## Running a feature-based molecular network on GNPS2

FBMN with Progenesis QI results can be performed using the [GNPS2 feature_based_molecular_networking_workflow](https://gnps2.org/workflowinput?workflowname=feature_based_molecular_networking_workflow): please refer to the [main FBMN documentation](fbmn.md) for more informations.


