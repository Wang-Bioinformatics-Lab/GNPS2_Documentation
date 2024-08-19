# Feature-Based Molecular Networking (FBMN)

## Introduction

**Feature-Based Molecular Networking** (FBMN) is a computational method that bridges popular mass spectrometry data processing tools for LC-MS/MS and molecular networking analysis on [GNPS2](https://gnps2.org). 

The main documentation for **Feature-Based Molecular Networking** is provided below. See [the Nature Methods article here](https://www.nature.com/articles/s41592-020-0933-6).

The Feature-Based Molecular Networking (FBMN) workflow is available on GNPS2 [here](https://gnps2.org/workflowinput?workflowname=feature_based_molecular_networking_workflow) (you need to be logged in GNPS2 first). 


- For programmatic access to FBMN, contact Mingxun Wang at <mingxun.wang@ucr.edu>.

## Citations

!!! quote "Recommended Citations"
    This work builds on the efforts of our many colleagues, please make sure to cite the papers for their processing tools and the following GNPS papers

    Nothias, L.-F., Petras, D., Schmid, R. et al. [Feature-based molecular networking in the GNPS analysis environment](https://www.nature.com/articles/s41592-020-0933-6). Nat. Methods 17, 905–908 (2020).

    Wang, M. et al. [Sharing and community curation of mass spectrometry data with Global Natural Products Social Molecular Networking](https://doi.org/10.1038/nbt.3597). Nat. Biotechnol. 34, 828–837 (2016).

## Mass Spectrometry Data Processing for the FBMN

In brief, popular mass spectrometry processing programs have been adapted to export two files (*feature quantification table* and *MS/MS spectral summary*) files that can be used with the Feature Based Molecular Networking (FBMN) workflow on GNPS. Alternatively, the FBMN supports the mzTab-M format that can be inputted along witht the mzML file(s). The tools supported and their main features are presented in the table below along with a step-by-step documentation to use in FBMN on GNPS:

|  Processing tool | Doc.| Data supported | Interface | Platform | Code |Target user|
|---|---|---|---|---|---|---|
|[MZmine](https://github.com/mzmine/mzmine2/)|Doc in preparation | Non-targeted LC-MS/MS | Graphical UI|Any|[Open source](https://github.com/mzmine/mzmine2/blob/master/LICENSE.txt)|Mass spectrometrists|
|[MS-DIAL](https://systemsomicslab.github.io/compms/index.html)|Doc in preparation | Non-targeted LC-MS/MS, **MSE**, **Ion Mobility** | Graphical UI|Windows|[Open source](https://systemsomicslab.github.io/compms/index.html)|Mass spectrometrists|
|[OpenMS](https://github.com/OpenMS/OpenMS/)|Doc in preparation| Non-targeted LC-MS/MS |Commandline|Any|[Open source](https://github.com/OpenMS/OpenMS/blob/develop/License.txt)|Bioinformaticians and developers|
|[XCMS](https://github.com/sneumann/xcms)|Doc in preparation | Non-targeted LC-MS/MS |Commandline|Any|[Open source](https://github.com/sneumann/xcms)|Bioinformaticians and developers|
|[MetaboScape](https://www.bruker.com/en/products-and-solutions/mass-spectrometry/ms-software/metaboscape.html)|Doc in preparation| Non-targeted LC-MS/MS, **Ion Mobility** |Graphical UI|Windows|Proprietary code|Mass spectrometrists|
|[Progenesis QI](http://www.nonlinear.com/progenesis/qi/)|[See doc.](FBMN-with-progenesisQI.md)| Non-targeted LC-MS/MS, **MSE**, **Ion Mobility** |Graphical UI|Windows|Proprietary code|Mass spectrometrists|
|[mzTab-M](https://pubs.acs.org/doi/abs/10.1021/acs.analchem.8b04310)|Doc in preparation| Non-targeted LC-MS/MS | Standardized format|Multi-systems|[Open source](https://github.com/lifs-tools/jmzTab-m)|All public|

**IMPORTANT:** The software used for the LC-MS/MS data processing has to be configured and utilized as recommended by its documentation.

## The FBMN Workflow in GNPS2

There is a dedicated Feature-Based Molecular Networking workflow on GNPS2 that [can be accessed here](https://gnps2.org/workflowinput?workflowname=feature_based_molecular_networking_workflow) (you need to be logged in GNPS2 first).

### Requirement for the FBMN workflow
After processing your LC-MS/MS data with the prefered software, it is possible to export the results into 3 input files for FBMN:

1. A *feature table* with the intensities of LC-MS ion features (TXT or CSV format).
1. A *MS/MS spectral summary* file with a list of MS/MS spectra associated with the LC-MS ion features (.MGF file or .msp file).
3. [Optional] *Metadata table* - format described [here](link to be added)
