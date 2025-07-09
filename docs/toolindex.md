# GNPS2 Tool Index

This is a global tool index for GNPS2. Throughout this documentation we have very detailed information for how to use way more tools than we thought we'd have, but it's a good problem to have!

However, we recognize it might be difficult for people to simply see what all is available in GNPS as tool and web services. This table is always evolving and hope to make it easier for people to navigate. 

Please help us fill in more completely!


## GNPS2 Web Tools

These are web tools that is run by the GNPS2 team and provides complementary functionality to GNPS2. 

| Tool                                                                               | Documentation           | Source Code                                                                         | Citation                                                                |
|------------------------------------------------------------------------------------|-------------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Pubmed Co-Authors List](https://coauthor.wanglab.science/)                        | ---                     | ---                                                                                 | ---                                                                     |
| [Nature Journals Author Quick Entry](https://natureauthors.wanglab.science/)       | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Spectral Similarity Hub](https://similarity.gnps2.org/)                     | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Structure Server](https://structure.gnps2.org/)                             | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Cytoscape](https://cytoscape.gnps2.org/)                                    | ---                     | ---                                                                                 | ---                                                                     |
| [Metabolomics Spectrum Resolver](https://metabolomics-usi.gnps2.org)               | [Documentation](usi.md) | [GitHub](https://github.com/mwang87/MetabolomicsSpectrumResolver)                   | [Citation](https://www.biorxiv.org/content/10.1101/2020.05.09.086066v1) |
| [GNPS2 Networking URL Formatter](https://urlformatter.gnps2.org)                   | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Classical Networking Upset Plot Dashboard](http://classicalupset.gnps2.org/) | ---                     | [GitHub](https://github.com/mwang87/GNPS_ClassicalNetworkGroupsComparisonDashboard) | ---                                                                     |
| [GNPS2 FBMN Upset Plot Dashboard](https://fbmnupset.gnps2.org/)                    | ---                     | ---                                                                                 | ---                                                                     |
| [NP Classifier](https://npclassifier.gnps2.org/)                                   | ---                     | [GitHub](https://github.com/mwang87/NP-Classifier)                                  | ---                                                                     |
| [GNPS2 Dashboard](https://dashboard.gnps2.org/)                                    | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Plotter Dashboard (Beta)](https://plotter.gnps2.org/)                       | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Dataset File Explorer (Beta)](https://explorer.gnps2.org/)                  | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Public Libraries Download List](https://external.gnps2.org/gnpslibrary)     | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Tiny Mass Sharer](https://tinymass.gnps2.org/)                              | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 MassQL Visualizer](https://massql.gnps2.org/)                               | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 MassQL Analysis/Chatbot](https://massql-analysis.gnps2.org/)                | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 USI Playground](https://usi-playground.gnps2.org/)                          | ---                     | ---                                                                                 | ---                                                                     |
| [GNPS2 Network Customization Playground](https://networkcustomization.gnps2.org/)  | ---                     | ---                                                                                 | ---                                                                     |
| [RDD App](https://gnps-rdd.streamlit.app/)                                         | ---                     | ---                                                                                 | ---                                                                     |
| [FBmnStatsGUIde](https://fbmn-statsguide.gnps2.org/)                               | ---                     | [GitHub](https://github.com/Functional-Metabolomics-Lab/FBMN-STATS)                 | ---                                                                     |
| [Chemical Proportionality](https://chemprop.gnps2.org/)                            | ---                     | ---                                                                                 | ---                                                                     |
| [CorrOmics](https://corromics.gnps2.org/)                                          | ---                     | ---                                                                                 | ---                                                                     |
| [Conjugated Metabolome Explorer](https://conjugated-metabolome.streamlit.app/)     | ---                     | ---                                                                                 | ---                                                                     |
| [CMMC Batch validation](https://cmmc-validation.gnps2.org/)                        | ---                     | [GitHub](https://github.com/Wang-Bioinformatics-Lab/streamlit-cmmc-validator)       | ---                                                                     |
| [MetaboApp - Reverse Metabolomics](https://reversemetabolomics.streamlit.app/)     | ---                     | ---                                                                                 | ---                                                                     |
| [MetaboApp - DrugReadouts](https://drugreadouts.gnps2.org/)                        | ---                     | [GitHub](https://github.com/wilhan-nunes/streamlit_drug_readouts)                   | ---                                                                     |
| [MetaboApp - CMMC Dashboard](https://cmmc-dashboard.gnps2.org/)                    | ---                     | [GitHub](https://github.com/wilhan-nunes/streamlit_CMMC_analysis-dashboard)         | ---                                                                     |
| [MetaboApp - MassQL Post-MN](https://massqlpostmn.gnps2.org/)                      | ---                     | [GitHub](https://github.com/helenamrusso/streamlit-massql-post-mn)                  | ---                                                                     |
| [MetaboApp - Multi‑step MassQL](https://multi-step-massql.streamlit.app/)          | ---                     | ---                                                                                 | ---                                                                     |


## Web Interfaces Description

### MassQL Post-MN

Enables users to perform spectral pattern-based queries directly on post-processed GNPS molecular networking outputs using the MassQL language.

[MassQL Post-MN](https://massqlpostmn.gnps2.org/)

### Multi-step MassQL

Allows construction of sequential MassQL queries, useful for identifying structurally related molecules (e.g., distinguishing isomers) through compound-specific fragmentation patterns.

[Multi-step MassQL](https://multi-step-massql.streamlit.app/)

### RDD App

Summarizes molecular networking results by integrating ontology annotations and sample metadata, helping contextualize chemical features within biological or experimental frameworks.

[RDD App](https://gnps-rdd.streamlit.app/)

### Food Readout

Annotates molecular features with dietary ontology terms, enabling exploration of potential food-derived metabolite exposures in untargeted metabolomics data.

[Food Readout](https://foodreadouts.streamlit.app/)

### Drug Readout

Maps chemical features to standardized pharmacological vocabularies to identify drug-derived signals in complex datasets.

[Drug Readout](https://drugreadouts.gnps2.org/)

### CMMC Dashboard

Visualizes enrichment analyses using the Collaborative Microbial Metabolite Center (CMMC) knowledgebase, linking features to known microbial metabolic products.

[CMMC Dashboard](https://cmmc-dashboard.gnps2.org/)


### FBMN Stats

Offers statistical analysis tools tailored for Feature-Based Molecular Networking (FBMN) outputs, including differential abundance and multivariate assessments.

[FBMN Stats](https://fbmn-statsguide.gnps2.org/)

### Chemical Proportionality

Analyzes relative abundance trends of structurally related compounds to infer biochemical transformations or metabolic dependencies.

[Chemical Proportionality](https://chemprop.gnps2.org/)

### CorrOmics

Supports correlation-based multi-omics integration, linking metabolomics features to other data types such as genomics or transcriptomics.

[CorrOmics](https://corromics.gnps2.org/)

### Conjugated Metabolome Explorer

Facilitates the exploration of metabolite conjugation patterns across large datasets, aiding the identification of phase II metabolism products.

[Conjugated Metabolome Explorer](https://conjugated-metabolome.streamlit.app/)

### Reverse Metabolomics

Enables querying of large repositories to identify metadata or sample types associated with specific molecular features, providing reverse-lookup functionality for biomarker discovery.

[Reverse Metabolomics](https://reversemetabolomics.streamlit.app/)


### MS/MS Spectrum Summary App

Here is a little app that can take a set of MS/MS spectra and understand the consistent fragmentation.

[Spectrum Summary App](https://spectrasummary.gnps2.org/)

### Molecular Networking Reformatting App

This little app can reformat molecular networking outputs to create tall tables to make downstream analysis a bit easier. 

[Networking Reformatting App](https://networkcustomization.gnps2.org/second_page)

### Coauthor Summarizer

This app can take all of your publications and tell you who your coauthors were in the last n years. Pretty useful for NSF proposals. 

[Coauthor App](https://coauthor.wanglab.science/)

### TinyMass App

This app is like tinyurl but for mass spectra. You can easily share MS spectra and get a USI that can be used in a ton of different places

[TinyMass App](https://tinymass.gnps2.org/)

### USI Generation App

This app will help to create USIs from a variety of places from datasets to GNPS2 analysis jobs. Making it easier to interact with the rest of the ecosystem. 

[USI Generation App](https://usi-playground.gnps2.org/)

### MassQL Analysis App

This app makes working with MassQL a lot easier. 

You can do the following:

1. Play around with MassQL against MS/MS spectral libraries
2. Use an LLM to write and interact with MassQL queries for the first time
3. Use an LLM to explain the MassQL Queries 

[MassQL Analysis App](https://massql-analysis.gnps2.org/)


## GNPS2 Jupyter Notebooks

These notebooks are for postprocessing of results from GNPS/GNPS2 and other computational processing that have not been integrated yet. If they are super useful, we can integrate into high throughput workflows. For now, give them a try!

| Tool | Documentation | Source Code | Binder Launch |
| ---- | ------------- | ----------- | ------------- |
| GNPS2 MASST Post Processing | --- | [GitHub](https://github.com/mwang87/GNPS_MASST_Notebooks) | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mwang87/GNPS_MASST_Notebooks/master?labpath=src%2Fjupyternotebook.ipynb) |
| GNPS2 MassQL and Networking Integration | --- | [GitHub](https://github.com/Wang-Bioinformatics-Lab/MassQL_Networking_Connection_Notebook) | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Wang-Bioinformatics-Lab/MassQL_Networking_Connection_Notebook/master?labpath=src%2Fjupyternotebook.ipynb) |
| GNPS2 Networking Family Consistent Fragmentation | --- | [GitHub](https://github.com/Wang-Bioinformatics-Lab/MolecularFamily_Consistent_Fragmentation_Notebook) | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Wang-Bioinformatics-Lab/MolecularFamily_Consistent_Fragmentation_Notebook/master?labpath=src%2Fjupyternotebook.ipynb) |
| GNPS2 MassQL Post Processing | --- | [GitHub](https://github.com/Wang-Bioinformatics-Lab/MassQL_Workflow_Postprocessing_Notebooks) | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Wang-Bioinformatics-Lab/MassQL_Workflow_Postprocessing_Notebooks/master?labpath=src%2Fjupyternotebook.ipynb) |
| CMMC Integration | --- | [GitHub](https://github.com/Wang-Bioinformatics-Lab/CMMC-GNPS-Integration-Notebook) | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Wang-Bioinformatics-Lab/CMMC-GNPS-Integration-Notebook/master) |


## Community Tools GNPS2 Interfaces with

| Tool  | Publication |
|---|---|
| [MS2LDA.org](http://ms2lda.org/) | [Citation](https://academic.oup.com/bioinformatics/article/34/2/317/4158166) |
| [NPAtlas](https://www.npatlas.org/joomla/) | [Citation](https://pubs.acs.org/doi/10.1021/acscentsci.9b00806) |
| [MIBiG](https://mibig.secondarymetabolites.org/) | [Citation](https://academic.oup.com/nar/article/48/D1/D454/5587631) |
| [ClassyFire](http://classyfire.wishartlab.com/) | [Citation](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-016-0174-y) |
| [SMART NMR](http://smart.ucsd.edu) | [Citation](https://pubs.acs.org/doi/abs/10.1021/jacs.9b13786) |
| MassBank | [Citation](https://onlinelibrary.wiley.com/doi/full/10.1002/jms.1777?casa_token=Wr51kpu9hCgAAAAA%3AERBV24GFextLVnW0J4SDcdJAskSYG2eqf2tgh8AUBeowVLnKBErbLqJxEzOQJUz2MqrI5dKr47zSVXw) |
| Cytoscape | [Citation](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC403769/) |
| ProteoWizard | [Citation](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2732273/) |
| [SNAP-MS](https://www.npatlas.org/discover/snapms/) | [Citation](https://www.nature.com/articles/s41467-022-35734-z) and [Documentation](https://liningtonlab.github.io/snapms_documentation/) |
