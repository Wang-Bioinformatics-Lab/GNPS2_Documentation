# Pan-ReDU

Welcome to **Pan-ReDU**!

## What is Pan-ReDU
**Finding and reusing data is hard.** ReDU aims to make that easier. ReDU is a community-focused approach to find and reuse public data containing mass spectrometric data at the repository scale. It is a collection of metadata from [MetaboLights](https://www.ebi.ac.uk/metabolights/index), [Metabolomics Workbench](https://www.metabolomicsworkbench.org), and [GNPS/MassIVE](https://gnps.ucsd.edu/ProteoSAFe/datasets.jsp#%7B%22query%22%3A%7B%7D%2C%22table_sort_history%22%3A%22createdMillis_dsc%22%2C%22title_input%22%3A%22GNPS%22%7D) within a single table with harmonized nomenclature. Our goal is to empower researchers to contextualize their data with public data and explore questions using repository-scale public data.

## Components
There are three main components of Pan-ReDU to understand:

1. **Understanding and navigating public metadata**
    - The Pan-ReDU dashboard is available [here](https://redu.gnps2.org/selection/). Documentation on navigating the dashboard can be found on the following pages.
    - Explanations of metadata categories can be found [here](https://docs.google.com/spreadsheets/d/10U0xnJUKa_mD0H_9suH1KJAlJD9io9e4chBX8EAHneE/edit?gid=1856413163#gid=1856413163).
    - Allowed terms for each category are available [here](https://docs.google.com/spreadsheets/d/10U0xnJUKa_mD0H_9suH1KJAlJD9io9e4chBX8EAHneE/edit?gid=155945972#gid=155945972).

2. **Contributing public metadata** 
    - Tools for [validating](https://docs.google.com/spreadsheets/d/10U0xnJUKa_mD0H_9suH1KJAlJD9io9e4chBX8EAHneE/edit?gid=1001603307#gid=1001603307) and [submitting](https://deposit.redu.gnps2.org/) metadata are explained on the following pages.

3. **Downloading raw data**
    - Given a dataset accession id (e.g. MSV000083665, MTBLS284 or ST002962) download raw data file-by-file through the [GNPS2 Dataset Explorer](https://explorer.gnps2.org/) from any supported repository, as explained on the following pages.
    - Given a universal spectrum identifier (USI) (e.g. mzspec:MSV000083756:ccms_peak/Blank-3ACN-3IPA-2H2O_RE11_196.mzML) download raw data file-by-file through the [GNPS Dashboard](https://dashboard.gnps2.org/) from any supported repository, as explained on the following pages.
    - Given a list of USIs download raw data in batch using our [downloadpublicdata tool](https://github.com/Wang-Bioinformatics-Lab/downloadpublicdata) from any supported repository, as explained on the following pages.

# Page Contributions
Yasin El Abiead (UCSD) and Mingxun Wang (UCR)
