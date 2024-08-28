## Protocol to perform FBMN and Overlay workflow on GNPS2 with Progenesis data

The general documentation for FBMN on GNPS2 can be found [here](docs/fbmn.md) and the documentation for FBMN with Progenesis can be found [here](docs/FBMN-with-progenesisQI.md).

In summary, you will need to perform the following steps:
1. Import and process the mass spectrometry data with Progenesis QI
2. Export the processing results (the feature table file and the .msp file). 
3. Upload the feature table file and the .msp file to [GNPS2](https://gnps2.org/homepage)
4. [Optional] Prepare and upload the metadata file to GNPS2 - Metadata file format described [here](docs/metadata.md).
5. Upload other optional input files (Supplementary Pairs and/or Original mzML Files) to GNPS2 if necessary. See [FBMN documentation](docs/fbmn.md).
6. Launch FBMN Workflows on GNPS2 by following the [FBMN documentation](docs/fbmn.md) or click [here](https://gnps2.org/workflowinput?workflowname=feature_based_molecular_networking_workflow).
7. Select the input files, including a feature table file, the spectral .msp file and other optional input files
8. Select PROGENESIS as the Feature Finding Tool.
9. Set the parameters or just use the default settings - see [FBMN documentation](docs/fbmn.md).
10. Click Submit Workflow and wait for the workflow to finish.
11. After the FBMN task finishes, click “Downstream Analysis - Overlay Custom Network” in the Downstream Analysis section.
12. The Input MGF File and Input GraphML File have already been pre-populated, you just need to select the Input Overlay File from the feature table file uploaded before. Please note, the headers of the columns to be used should not contain any white space and special characters. 
13. Provide the "Overlay Node ID Column Header", e.g., “row_ID” without quotation marks.
14. Click Submit Workflow and wait for the task to finish.
