The [GNPS2 Dataset Explorer](https://explorer.gnps2.org/) is a simple interface to enable users to list out and select all files from a public dataset or analysis task. 

It current supports the following data sources:

1. MassIVE Public Datasets
1. GNPS Public Datasets
1. Metabolights Public Datasets
1. Metabolomics Workbench Public Datasets
1. GNPS Analysis Data Files (LC and GC)
1. PRIDE Proteomics Public Datasets
1. ProteomXchange Public Datasets

## Listing Dataset Files

Once you have entered an accession, a set of files will appear in the table. You may select one or more files to visualize. You can select "Visualize Files" below to see them in the GNPS2 Dashboard of the underlying raw data. Or you can choose to network them in GNPS2 by clicking "Molecular Network Files at GNPS2". 

!!! note
    You may select to visualize all files if you do not want to select them. It is limited to the first 50 in the table, so if you filter the table, the it will trim down this 50. 

### Metadata

We attempt to gather metadata from several sources for public mass spectrometry data in MassIVE/GNPS. The metadata source can be selected in the "Metadata Source" dropdown menu. Only metadata sources available for the current dataset is shown. 

1. Default (MS information from run)
1. ReDU
1. MassIVE Metadata Uploads
1. Metabolights Study Information

Please note that only partial ReDU metadata will be shown here. For full metadata go to the [Pan-ReDU metadata selection dashboard](https://redu.gnps2.org/selection/).

## Listing GNPS Tasks

The Dataset Explorer will list out all the files selected in the GNPS analysis and attempts to pull in the metadata from the analysis as well. 
## Comparing Two Files for LCMS Viewer

There are two tables with identical entries right above/below one another. This enables easily to select two sets of files to visualize in the GNPS2 Dashboard. Simply put a check mark next to the files in each table you want to compare and select the "Visualize Files" button below. 

## Server Selection Feature 

We are excited to introduce our new server selection to the Dataset Explorer, giving users more control over their experience. This feature allows users to choose the server location of the dashboard, providing more flexibility and improving overall performance.

## Server status 
Currently we are supporting two locations where users can choose from:

1. UCR Riverside, America
1. University of Tübingen, Germany 


Detailed server status are shown below:

| Server              | Status |
|:-------------------:|:---------------------------------------------------------------:|
| **GNPS2 - USA-UCR** | [US Server](https://stats.uptimerobot.com/4P67vuzkr8/793055871) |
| **GNPS2 - DE-Tue**  | [DE Server](https://stats.uptimerobot.com/4P67vuzkr8/796180194) |

Feel free to share about your experiences with the new server selection and help us improving it further!
