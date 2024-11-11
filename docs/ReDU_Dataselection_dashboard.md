# Pan-ReDU Data Selection Dashboard User Guide

Welcome to the **Pan-ReDU Dashboard**! This guide will help you navigate the [dashboard](https://redu.gnps2.org/selection/), filter data, download datasets, and utilize downstream tools for your metabolomics research.

## Overview

The **Pan-ReDU Dashboard** is a comprehensive platform that aggregates metadata from public metabolomics repositories:

- **MetaboLights**
- **Metabolomics Workbench**
- **GNPS**

By consolidating this data, the dashboard provides a unified interface for exploring and analyzing metabolomics datasets.

## Navigation Bar

At the top of the dashboard, you'll find the navigation bar, which includes:

- **ReDU Logo**: Click to return to the homepage.
- **Contribute Your Data**: Link to [submission page](https://deposit.redu.gnps2.org/) for your own metadata.
- **ReDU Dashboard - Documentation**: Access detailed documentation about the dashboard.
- **Download Complete ReDU**: Download the entire ReDU dataset.

## Summary Statistics

On the left side of the dashboard, the **Summary Statistics** card provides quick insights:

- **Total Files**: Number of files available.
- **Unique Datasets**: Number of datasets.
- **Files by DataSource**: Breakdown of files by their source repository.
- **Represented Taxonomies**: Diversity of biological NCBI taxa represented.
- **Human/Mouse Data**: Specific statistics for human and mouse samples (often of interested for biomedical studies).
- **Last Modified**: Date when the dataset was last updated.

## Filtering Data

### Using Column Filters

Below the summary statistics, the main data table displays the dataset. Each column header includes a filter input:

1. **Locate the Column Filter**: Click on the filter input beneath the column name.
2. **Enter Filter Criteria**: Input your filter expression. You can use operators such as:
   - `=`: Equals (for numerical columns)
   - `!=`: Not equal (for numerical columns)
   - `>`: Greater than (for numerical columns)
   - `<`: Less than (for numerical columns)
   - `>=`: Greater than or equal to (for numerical columns)
   - `<=`: Less than or equal to (for numerical columns)
   - `contains`: Contains substring (for character columns; case-insensitive)
   - `scontains`: Contains substring (for character columns; case-sensitive)
3. **Apply Multiple Filters**: Combine filters using `&&` (AND operator). For example:

    **Example**: To find entries where "NCBITaxonomy" contains 'Homo sapiens' and "MassSpectrometer" contains 'Orbitrap' :
    
       ```sql
       {NCBITaxonomy} contains "Homo sapiens" && {MassSpectrometer} contains "Orbitrap"
       ```

4. **Regular Expressions in Filters**: Use regular expressions (regex) within the `contains` operator for complex filtering.

    **Example**: To find entries where `NCBITaxonomy` contains either "Homo" or "Mus", but not "musculus":

    ```sql
    {NCBITaxonomy} contains "(Homo|Mus)(?!.*musculus)"
    ```

    **Explanation**:

    - `(Homo|Mus)`: Matches "Homo" or "Mus".
    - `(?!.*musculus)`: Negative lookahead to exclude entries containing "musculus".

    **Example**: To find samples where `UBERONBodyPartName` contains "blood" and `NCBITaxonomy` contains "Rattus norvegicus":

    ```sql
    {UBERONBodyPartName} contains "blood" && {NCBITaxonomy} contains "Rattus norvegicus"
    ```

    ### Example Filters

    The dashboard provides preset example filters for quick access:

    - **Human Samples**: Filters for samples from *Homo sapiens*.
    - **Plant Samples**: Shows samples categorized under plants.
    - **Orbitrap Mass Spectrometer**: Filters samples analyzed using an Orbitrap mass spectrometer (QExactive, Orbitrap, Astral substrings).
    - **Homo sapiens and Mus but no Mus musculus**: Advanced filter excluding *Mus musculus*.
    - **Blood Samples from Rattus norvegicus**: Filters for blood samples from *Rattus norvegicus*.

    **To use an example filter**:

    1. **Click on the Filter Name**: Under "Example Filters", click the desired filter button.
    2. **View Filtered Data**: The data table will automatically update to reflect the filter.

    ### Subset to mz(X)ML Files

    To filter the table to only include files ending with `.mzML` or `.mzXML`:

    1. **Click "Subset Table to mz(X)ML files"**: This button is located under "Filter Table"-button. Make sure the USI column is not Toggled before clicking. 
    2. **View Results**: The data table will display only the relevant files while keeping your current filters.

    ## Downloading Data

    ### Download Filtered Data

    After applying your filters, you can download the resulting dataset:

    1. **Click "Download Filtered Table"**: Located under "Download selection".
    2. **Save the File**: A CSV file named `filtered_dataset.csv` will be downloaded to your device.

    ### Download Complete Dataset

    To download the entire ReDU dataset:

    - **Click "Download Complete ReDU"**: Found in the navigation bar at the top.

    ## Downstream Tooling

    The dashboard offers direct links to tools for further analysis:

    ### USIs → Molecular Networking

    - **Purpose**: Generate Molecular Networks for filtered files using Universal Spectrum Identifiers (USIs).
    - **Important Note**:
      - **Top 50 mz(X)ML Files**: When you click this link, the system selects the first 50 mz(X)ML files from your filtered data.
      - **Processing More USIs**: If you wish to process more USIs, please download the filtered table (as described above) to get the complete filtered table and copy the USIs directly into the [workflow](https://gnps2.org/workflowinput?workflowname=classical_networking_workflow).
    - **How to Use**:
      1. **Click "USIs → Molecular Networking"** under "Downstream tooling".
      2. **Proceed to GNPS**: You'll be redirected to the GNPS workflow input page with the USIs already populated.

    ### USIs → MassQL

    - **Purpose**: Query mass spectrometry data using [MassQL](https://mwang87.github.io/MassQueryLanguage_Documentation/).
    - **Important Note**:
      - **Top 50 mz(X)ML Files**: As with Molecular Networking, only the top 50 mz(X)ML files are used to prevent system overload.
      - **Processing More USIs**: If you wish to process more USIs, please download the filtered table (as described above) to get the complete filtered table and copy the USIs directly into the [workflow](https://gnps2.org/workflowinput?workflowname=massql_workflow).
    - **How to Use**:
      1. **Click "USIs → MassQL"**.
      2. **Proceed to GNPS**: You'll be taken to the MassQL workflow input page with the USIs already populated.

    ### USIs → Raw Data Download

    - **Purpose**: Download raw mass spectrometry data files.
    - **Important Note**:
      - **This returns a tsv file**: This link returns **all** USIs from your filtered selection in a tsv file not the actual raw data.
    - **How to Use**:
      1. **Click "USIs → Raw Data Download"**.
      2. **Download Data**: You'll download a tsv file with USIs of the filtered table. You will then be directed to the GitHub repository of the [commandline tool](https://github.com/Wang-Bioinformatics-Lab/downloadpublicdata) to download the raw data. The tutorial for that tool can be found here.

    ## Additional Features

    ### Customizing Columns

    - **Show/Hide Columns**:
      - **Select "Hide Column" or "Show Column"**: Customize which columns are visible.

# Page Contributions
Yasin El Abiead (UCSD), and Mingxun Wang (UCR)
