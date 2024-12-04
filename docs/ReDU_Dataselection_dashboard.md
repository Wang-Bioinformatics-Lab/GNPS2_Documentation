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

- **Pan-ReDU Logo**: Click to return to the homepage.
- **Contribute Your Data**: Link to [submission page](https://deposit.redu.gnps2.org/) for your own metadata.
- **Pan-ReDU Dashboard - Documentation**: Access detailed documentation about the dashboard.
- **Download Complete Pan-ReDU**: Download the entire Pan-ReDU dataset.


## Summary Statistics

On the left side of the dashboard, the **Summary Statistics** card provides quick insights:

- **Total Files**: Number of files available.
- **Unique Datasets**: Number of datasets.
- **Files by DataSource**: Breakdown of files by their source repository.
- **Represented Taxonomies**: Diversity of biological NCBI taxa represented.
- **Human/Mouse Data**: Specific statistics for human and mouse samples (often of interest for biomedical studies).
- **Last Modified**: Date when the dataset was last updated.


## Filtering Data

### Using Column Filters

Below the summary statistics, the main data table displays the dataset. Each column header includes a filter input:

1. **Locate the Column Filter**: Click on the filter input beneath the column name.
2. **Enter Filter Criteria**: Input your filter expression. You can use operators such as:
   - `=`: Equals (for numerical and character columns)
   - `!=`: Not equal (for numerical columns)
   - `>`: Greater than (for numerical columns)
   - `<`: Less than (for numerical columns)
   - `>=`: Greater than or equal to (for numerical columns)
   - `<=`: Less than or equal to (for numerical columns)
   - `contains`: Contains substring (for character columns; case-insensitive)
   - `scontains`: Contains substring (for character columns; case-sensitive)

3. **Apply Multiple Filters**: Combine filters using `&&` (AND operator). For example:

    **Example**: To find entries where "NCBITaxonomy" contains 'Homo sapiens' and "MassSpectrometer" contains 'Orbitrap':

    ```sql
    {NCBITaxonomy} contains "Homo sapiens" && {MassSpectrometer} contains "Orbitrap"
    ```

4. **Regular Expressions in Filters**: Use regular expressions (regex) within the `contains` operator for complex filtering.

    **Example**: To find entries where `NCBITaxonomy` contains either "Homo" or "Mus", but not "musculus":

    ```sql
    {NCBITaxonomy} contains "(Homo|Mus)(?!.*musculus)"
    ```

    **Example**: To find samples where `UBERONBodyPartName` contains "blood" and `NCBITaxonomy` contains "Rattus norvegicus":

    ```sql
    {UBERONBodyPartName} contains "blood" && {NCBITaxonomy} contains "Rattus norvegicus"
    ```

### Example Filters

The dashboard provides preset example filters for quick access. These filters are not meant to be exhaustive. For example, the Plant Samples filter will return all rows with value "plant" in the "SampleType" column rather than return all plant samples. For more complex filters (e.g., plant samples based on the NCBITaxonomy), download the whole dataset and do so locally or reach out to us:

- **Human Samples**: Filters for samples from *Homo sapiens*.
- **Plant Samples**: Shows samples categorized under plants.
- **Orbitrap Mass Spectrometer**: Filters samples analyzed using an Orbitrap mass spectrometer (QExactive, Orbitrap, Astral substrings).
- **Homo sapiens and Mus but no Mus musculus**: Advanced filter excluding *Mus musculus*.
- **Blood Samples from Rattus norvegicus**: Filters for blood samples from *Rattus norvegicus*.
- **Samples with RP-LC, hydrophobic extraction and MS2 scans**: Filters for files with MS/MS scans, hydrophobic extraction solvents, and reversed phase chromatography. (lipidomics type analysis)

**To use an example filter**:

1. **Click on the Filter Name**: Under "Example Filters", click the desired filter button.
2. **View Filtered Data**: The data table will automatically update to reflect the filter.

### Subset to mz(X)ML Files

To filter the table to only include files ending with `.mzML` or `.mzXML`:

1. **Click "Subset Table to mz(X)ML files"**: This button is located under "Filter Table". Make sure the USI column is not toggled before clicking.
2. **View Results**: The data table will display only the relevant files while keeping your current filters.


## Downloading Data

### Download Filtered Data

After applying your filters, you can download the resulting dataset by clicking **"ReDU Table"** which is located under "Download Filtered Subset".

### USIs for Batch Processing/Download

Download USIs of filtered ReDU table as tsv file which can be used for batch processing in various GNPS tools or raw data download.

**How to Use**:
  1. **Download Data**: You'll download a TSV file with USIs of the filtered table. You can download raw data for those USIs in batch via the [command-line tool](https://github.com/Wang-Bioinformatics-Lab/downloadpublicdata). The tutorial for that tool can be found [here](https://github.com/Wang-Bioinformatics-Lab/downloadpublicdata) and on the next pages of this documentation.
  2. **Batch Molecular Networking or MassQL search**: You can paste downloaded USIs directly into the text fields of the workflows for [MassQL](https://gnps2.org/workflowinput?workflowname=massql_workflow) or [Molecular Networking](https://gnps2.org/workflowinput?workflowname=classical_networking_workflow). If you do not have a GNPS2 account yet, reach out to Prof. Mingxun Wang.


!!! note
  **GNPS2 is a shared resource** where the sceintific community can gain access to computational resources free of cost. For this reason batch processing of thousands if files via the downstream tooling described below (especially MassQL and Molecular Networking) will likely fail due to insufficient resources. However, if you still wish to do so you can always download raw data as described below and clone the [Github Molecular Networking repository](https://github.com/Wang-Bioinformatics-Lab/Classical_Networking_Workflow) or [Github MassQL repository](https://github.com/Wang-Bioinformatics-Lab/MassQL_Workflow) to on your local computer. 

### Download Complete Dataset

To download the entire ReDU dataset click "Download Complete ReDU"** found in the navigation bar at the top.


## View/Download Raw Data in Browser

After selecting files via the row checkboxes you can view the selected raw data files directly in your browser or download them to your PC by chlicking the "View/Download Raw Data in Browser" button. This will redirect to the [GNPS dashboard](https://dashboard.gnps2.org/) input page with the USIs already populated.

!!! note
  **Raw data download**: If you wish to download raw data, scroll down to the 'File Summaries' section of the Dashboard and click the download buttons. 


## Downstream Tooling

### Molecular Networking/Library Matching

Generate Molecular Networks and molecule annotations for selected files.

!!! note
  **Batch processing**: If you wish to process more files than can be selected on a single page, download the (filtered) ReDU table, as described above, or the filtered USIs (via the "USIs for Batch Processing/Download" button) and copy the USIs directly into the text field of the [workflow](https://gnps2.org/workflowinput?workflowname=classical_networking_workflow).

### MassQL/Fragmentation Rule Search

Query mass spectrometry data using [MassQL](https://mwang87.github.io/MassQueryLanguage_Documentation/).

!!! note
  **Batch processing**: If you wish to process more files than can be selected on a single page, download the (filtered) ReDU table, as described above, or the filtered USIs (via the "USIs for Batch Processing/Download" button) and copy the USIs directly into the text field of the [workflow](https://gnps2.org/workflowinput?workflowname=massql_workflow).

## Additional Features

### Customizing Columns

*Select "Hide Column" or "Show Column"**: Customize which columns are visible.

# Page Contributions

Yasin El Abiead (UCSD), and Mingxun Wang (UCR)
