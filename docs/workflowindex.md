# GNPS2 Workflow Index

This is a workflow index for GNPS2. Throughout this documentation we have a small tutorial of the list of workflows listed [https://gnps2.org/workflows](https://gnps2.org/workflows)
The source code and the documentation of the tools will be linked at the beginning of each tool. 

The workflows are [nextflow](https://www.nextflow.io/docs/latest/getstarted.html) workflows that can be run independently in any server running nextflow. 

However, we recognize it might be difficult to keep this documentation up to date, so please help us fill in more completely! Edit online, submit the PR and we will review it!

## GNPS2 Workflows

### MS-MS chooser
| [Link](https://gnps2.org/workflowinput?workflowname=msms_choser_nextflow_workflow) | [Source Code](https://github.com/albertogilf/nextflow_msms-choser) | [Tool documentation](https://ccms-ucsd.github.io/GNPSDocumentation/msmschooser/) | ---  |
| :--- | :--- | :--- | :--- |

MSMS-Chooser is a GNPS2 workflow and open-source protocol to empower the community to collect MS/MS reference data and contribute to the public MS/MS reference library. 
This specific step enables the finding of reference MS/MS spectra automatically in LC/MS data of pure standards given the structure of the pure standards. 

Input:
Annotations file in .tsv format from MassIVE. 
Spectra path containing a set of mzML/XML files. 
tolerance: in ppm

Output: 
A .tsv file with the extracted information spectra from the molecule of interest. 


### Feature-based Molecular Networking
| [Link](https://gnps2.org/workflowinput?workflowname=feature_based_molecular_networking_workflow) | --- | [Tool documentation](fbmn.md) | ---  |
| :--- | :--- | :--- | :--- |

### NP-Classifier
| [Link](https://gnps2.org/workflowinput?workflowname=NP_Classifier_nextflow_workflow) | [Source Code](https://github.com/albertogilf/nextflow_NP-Classifier) | [Tool documentation](https://github.com/albertogilf/nextflow_NP-Classifier) | ---  |
| :--- | :--- | :--- | :--- |

### MS2LDA
| [Link](https://gnps2.org/workflowinput?workflowname=ms2lda_nextflow_workflow) | [Source Code](https://github.com/glasgowcompbio/pySubstructures) | [Tool documentation](https://ms2lda.org/user_guide/) | [Citation](https://academic.oup.com/bioinformatics/article/34/2/317/4158166)  |
| :--- | :--- | :--- | :--- |

### ChemWalker
| [Link](https://gnps2.org/workflowinput?workflowname=chemwalker_nextflow_workflow) | [Source Code](https://github.com/computational-chemical-biology/ChemWalker/tree/master) | [Tool documentation](chemwalker_doc.md) | [Citation](https://academic.oup.com/bioinformatics/article/39/3/btad078/7067745?login=true)  |
| :--- | :--- | :--- | :--- |

### MS2query
| [Link](https://gnps2.org/workflowinput?workflowname=ms2query_nextflow_workflow) | [Source Code](https://github.com/iomega/ms2query/tree/main) | [Tool documentation](ms2query_doc.md) | [Citation](https://www.nature.com/articles/s41467-023-37446-4)  |

### MSHub-gc
| [Link](https://gnps2.org/workflowinput?workflowname=mshubgc_workflow) | [Source Code](https://github.com/Wang-Bioinformatics-Lab/mshub-gc_workflow) | [Tool documentation](mshub-gc_doc.md) | ---  |
| :--- | :--- | :--- | :--- |


<details>
<summary>## Genomics & Genome Mining Workflows on GNPS2</summary>

These workflows focus on genomic and metagenomic analysis, ranging from species identification and taxonomic profiling to genome mining for specialized metabolites.

---

### FastANI / pyANI
| [Link](https://gnps2.org/workflowinput?workflowname=FastANI) | [Tool documentation](https://github.com/ParBLiSS/FastANI) | [Citation](https://doi.org/10.1038/s41467-018-07641-9) | **Prod & Beta** |
| :--- | :--- | :--- | :--- |

These tools compute the **Average Nucleotide Identity (ANI)** between genomes, which is the current "gold standard" for defining bacterial species. While **FastANI** is optimized for speed and large-scale datasets using an alignment-free MinHash approach, **pyANI** provides a versatile framework for multiple ANI algorithms and visualization. 

### fastAAI
| [Link](https://gnps2.org/workflowinput?workflowname=fastAAI) | [Tool documentation](https://github.com/cruizperez/FastAAI) | [Citation](https://academic.oup.com/nar/article/53/8/gkaf348/8120557) | **Prod & Beta** |
| :--- | :--- | :--- | :--- |

An ultrafast estimator of whole-genome Average Amino Acid Identity (AAI). It is designed to scale to hundreds of thousands of genomes, allowing for rapid taxonomic placement and the exploration of evolutionary relationships across vast genomic databases.

### EzAAI
| [Link](https://gnps2.org/workflowinput?workflowname=EzAAI) | [Tool documentation](https://github.com/endixk/EzAAI) | [Citation](https://doi.org/10.1007/s12275-021-1154-0) | **Prod** |
| :--- | :--- | :--- | :--- |

A standalone tool for calculating the Average Amino Acid Identity (AAI) between two genomes. It provides a reliable metric for determining genus-level and family-level relationships where nucleotide similarity is no longer informative.

### antiSMASH
| [Link](https://gnps2.org/workflowinput?workflowname=antismash_workflow) | [Tool documentation](https://docs.antismash.secondarymetabolites.org/) | [Citation 1](http://dx.doi.org/10.1093/nar/gkr466), [Citation 2](https://doi.org/10.1093/nar/gkaf334) | **Beta** |
| :--- | :--- | :--- | :--- |

The "antibiotics and Secondary Metabolite Analysis Shell" is the premier tool for identifying **Biosynthetic Gene Clusters (BGCs)** in genomic data. It predicts the chemical structure of potential natural products by analyzing the enzymatic domains present in a genome.

### ONT EMU
| [Link](https://gnps2.org/workflowinput?workflowname=ont_emu_workflow) | [Tool documentation](https://github.com/treangenlab/emu) | [Citation](https://doi.org/10.1038/s41592-022-01520-4) | **Prod & Beta** |
| :--- | :--- | :--- | :--- |

Designed specifically for long-read sequencing (Oxford Nanopore), this workflow uses the **Emu** algorithm to perform species-level taxonomic profiling. It is highly effective for full-length 16S rRNA analysis, correcting for sequencing errors to provide high-resolution microbial community profiles.

### 16S rRNA Extraction
| [Link](https://gnps2.org/workflowinput?workflowname=16s_rrna_extraction) | [Tool documentation](https://github.com/tseemann/barrnap) | [Citation](https://doi.org/10.1093/bioinformatics/btq033) | **Beta** |
| :--- | :--- | :--- | :--- |

A targeted workflow for scanning whole-genome sequences or metagenomic assemblies to identify and extract the 16S ribosomal RNA gene sequences. It utilizes **barrnap** for rapid ribosomal RNA prediction and **BEDTools** for efficient genomic feature comparison.

</details>