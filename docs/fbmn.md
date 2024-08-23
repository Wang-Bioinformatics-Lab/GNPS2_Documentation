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

In brief, popular mass spectrometry processing programs have been adapted to export two files (*feature quantification table* and *MS/MS spectra file*) files that can be used with the Feature Based Molecular Networking (FBMN) workflow on GNPS. Alternatively, the FBMN supports the mzTab-M format that can be inputted along witht the mzML file(s). The tools supported and their main features are presented in the table below along with a step-by-step documentation to use in FBMN on GNPS:

|  Processing tool | Doc.| Data supported | Interface | Platform | Code |Target user|
|---|---|---|---|---|---|---|
|[MZmine](https://github.com/mzmine/mzmine2/)| Doc in preparation | Non-targeted LC-MS/MS | Graphical UI|Any|[Open source](https://github.com/mzmine/mzmine2/blob/master/LICENSE.txt)|Mass spectrometrists|
|[MS-DIAL](https://systemsomicslab.github.io/compms/index.html)| Doc in preparation | Non-targeted LC-MS/MS, **MSE**, **Ion Mobility** | Graphical UI|Windows|[Open source](https://systemsomicslab.github.io/compms/index.html)|Mass spectrometrists|
|[OpenMS](https://github.com/OpenMS/OpenMS/)| Doc in preparation| Non-targeted LC-MS/MS |Commandline|Any|[Open source](https://github.com/OpenMS/OpenMS/blob/develop/License.txt)|Bioinformaticians and developers|
|[XCMS](https://github.com/sneumann/xcms)| Doc in preparation | Non-targeted LC-MS/MS |Commandline|Any|[Open source](https://github.com/sneumann/xcms)|Bioinformaticians and developers|
|[MetaboScape](https://www.bruker.com/en/products-and-solutions/mass-spectrometry/ms-software/metaboscape.html)| Doc in preparation| Non-targeted LC-MS/MS, **Ion Mobility** |Graphical UI|Windows|Proprietary code|Mass spectrometrists|
|[Progenesis QI](http://www.nonlinear.com/progenesis/qi/)|[Documentation](FBMN-with-progenesisQI.md)| Non-targeted LC-MS/MS, **MSE**, **Ion Mobility** |Graphical UI|Windows|Proprietary code|Mass spectrometrists|
|[mzTab-M](https://pubs.acs.org/doi/abs/10.1021/acs.analchem.8b04310)| Doc in preparation | Non-targeted LC-MS/MS | Standardized format|Multi-systems|[Open source](https://github.com/lifs-tools/jmzTab-m)|All public|

**IMPORTANT:** The software used for the LC-MS/MS data processing has to be configured and utilized as recommended by its documentation.

## The FBMN Workflow in GNPS2

There is a dedicated Feature-Based Molecular Networking workflow on GNPS2 that [can be accessed here](https://gnps2.org/workflowinput?workflowname=feature_based_molecular_networking_workflow) (you need to be logged in GNPS2 first).

### Requirement for the FBMN workflow
After processing your LC-MS/MS data with the prefered software, it is possible to export the results into 2 required input files and 3 optional input files for FBMN:

1. A *feature table* with the intensities of LC-MS ion features (TXT or CSV format).
1. A *MS/MS spectral summary* file with a list of MS/MS spectra associated with the LC-MS ion features (.MGF file or .msp file).
3. [Optional] *Metadata table* - format described [here](metadata.md)
4. [Optional] *"Supplementary Pairs"* of additional edges - described [here](#advanced-extras) 
5. [Optional] *Original mzML Files* - These are the original files used for feature finding - described [here](#mzml-files-used-for-feature-finding)
   
### Upload the feature table file, the MS/MS spectral summary file and the optional Metadata tabole to GNPS2
Go to [GNPS2](https://gnps2.org/homepage) and click “File Browser” on the upper right corner, and then create a folder and drag and drop the feature table file, the spectral summary file and the optional metadata file to the folder. Alteratively You can also use the upload button to choose and upload the files.

### Launch FBMN Workflows on GNPS2
At [GNPS2 homepage](https://gnps2.org/homepage) click “Launch Workflows”, find “feature_based_molecular_networking_workflow”, then click “Launch Workflow”. 

#### Input File Select
1. Use “Select Input Inputfeatures” to select the feature table file as “Input inputfeatures”.
2. Use “Select Input Inputspectra” to select the MS/MS spectral summary file  (.mgf or .MSP) as “Input inputspectra”.
3. Use “Select Input Metadata File” to select the the optional metadata file as “Input Metadata File” if necessary.
4. Use "Select Input Spectral Library Folder" to select the spectral library as "Input Spectral Library Folder".
5. Use “Feature Finding Tool” to select "MZMINE, “PROGENESIS” or any other program that was used to generate the feature table and spectral summary files.

### Additional Edges
1. Use "Select Input Additional Supplemental Edges File(s) (Optional)" to select the optional *"Supplemental Pairs"* file(s)

### Raw Data Selection
1. Use "Input Raw Data Folder (Optional)" to select the optional *"Original mzML Files"*


### General Parameters
| Parameter  | Description          | Default |
| ------------- |-------------| -----|
| Precursor Ion Mass Tolerance (PIMT) | Parameter used for spectral library search expressed in Daltons. Note that the value of this parameters should be consistent with the capabilities of the mass spectrometer and the specific instrument method used to generated the MS/MS data. Recommended Values value is ± 0.02 Da for high-resolution instruments (q-TOF, q-Orbitrap) and ± 2.0 Da for low-resolution instruments (ion traps, QqQ).| 2.0 |
| Fragment Ion Mass Tolerance (FIMT)	      | Parameters used for molecular networking and MS/MS spectral library searches. This value specifies how much fragment ions can be shifted from their expected m/z values. Recommended Values value is ± 0.02 Da for high-resolution instruments (q-TOF, q-Orbitrap) and ± 0.5 Da for low-resolution instruments (ion traps, QqQ). | 0.5 |

### Advanced Filtering Parameters
| Parameter        | Description          | Default
| ------------- |-------------| -----|
| Minimum Peak Intensity | All fragment ions in the MS/MS spectra below this raw intensity value will be deleted. By default, the filtering is disabled. | 0  |
| Precursor Window Filter | All peaks in a +/- 17 Da around precursor ion mass are deleted. Enabled by default. This removes the residual precursor ion, which is frequently observed in MS/MS spectra acquired on qTOFs. | Filter | |
| Window Filter | Filter out peaks that are not in the top 6 most intense peaks in a +/- 50Da window | Filter |

### Networking Parameters
| Parameter        | Description          | Default |
| ------------- |-------------| -----|
| min_cosine | Minimum cosine similarity score that two MS/MS spectra should get in order to be considered as connected in the network. | 0.7 |
| min_matched_peaks | Minimum number of common and shifted fragment ions that MS/MS spectra should contain in order to be considered as connected in the network. Default value is 6, but note that this parameters should be tuned depending on the molecules of interest, and the experimental conditions (such as the ionization mode and the fragmentation conditions). For example, the collision-induced fragmentation of some lipids produce only a few fragment ions. | 6 |
| networking_max_shift | Maximum mass shift between the precursor m/z values of two spectra in the network | 1999 (Da)|

### Advanced Spectral Library Search Options

| Parameter        | Description          | Default |
| ------------- |-------------| -----|
| Library Minimum Cosine |Minimum cosine score that MS/MS spectra should get in spectral matching with MS/MS spectral libraries in order to be considered an annotation.| 0.7 |
| Library Minimum Matched Peaks | Minimum number of common fragment ions that MS/MS spectra should contain in order to be considered for spectral library annotation. Default value is 6, but note that this parameters should be tuned depending on the molecules of interest, and the experimental conditions (such as the ionization mode and the fragmentation conditions). For example, the collision-induced fragmentation of some lipids produce only a few fragment ions. A lower value will allow clustering of MS/MS spectra containing less  fragment ions, however it will also induce clustering of MS/MS spectra from different molecular types to be connected in one network. A higher value will do the opposite| 6 |
| Analog Search |Whether to search data for analogs to library spectra| No |
| Top-K |Number of matches to report for each feature| 1 |

#### Advanced Extras

"Supplementary Pairs" is an option to add extra edges to the resulting FBMN. It was initially implemented for the Ion Identity Networking (IIN) workflow. The IIN supports currently MZmine, XCMS-CAMERA, and MS-DIAL. However, this approach is designed to stimulate the development and testing of new workflows as the input is an edge file in a generic CSV format. An edge is described by the following table:

| Header        | Description |
| ------------- |-------------|
| ID1 | Node ID 1 matching the row IDs |
| ID2 | Node ID 2 matching the row IDs |
| EdgeType | Any string describing the type of edge |
| Score | A numerical value for the score (cannot be empty) |
| Annotation | A string annotation |

Note that if Supplementary Pairs from other software are used, it is mandatory that the as the LC-MS feature identifier (ID) matches the "SCANS=" number in the MGF file.


#### mzML Files Used for Feature Finding

The original mzML/mzXML files that were used for feature finding can also be included. This provides a way for the workflow to link back to the original files and help people explore the data interactively. 

