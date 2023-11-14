# GNPS2 Workflow Index

This is a workflow index for GNPS2. Throughout this documentation we have a small tutorial of the list of workflows listed [https://gnps2.org/workflows](https://gnps2.org/workflows)
The source code and the documentation of the tools will be linked at the beginning of each tool. 

The workflows are [nextflow](https://www.nextflow.io/docs/latest/getstarted.html) workflows that can be run independently in any server running nextflow. 

However, we recognize it might be difficult to keep this documentation up to date, so please help us fill in more completely! Edit online, submit the PR and we will review it!

## GNPS2 Workflows

### MS-MS chooser
| [Link](https://gnps2.org/workflowinput?workflowname=msms_choser_nextflow_workflow) | [Source Code](https://github.com/albertogilf/nextflow_msms-choser) | [Tool documentation](https://ccms-ucsd.github.io/GNPSDocumentation/msmschooser/) | ---  |

MSMS-Chooser is a GNPS2 workflow and open-source protocol to empower the community to collect MS/MS reference data and contribute to the public MS/MS reference library. 
This specific step enables the finding of reference MS/MS spectra automatically in LC/MS data of pure standards given the structure of the pure standards. 

Input:
Annotations file in .tsv format from MassIVE. 
Spectra path containing a set of mzML/XML files. 
tolerance: in ppm

Output: 
A .tsv file with the extracted information spectra from the molecule of interest. 

### NP-Classifier
| [Link](https://gnps2.org/workflowinput?workflowname=NP_Classifier_nextflow_workflow) | [Source Code](https://github.com/albertogilf/nextflow_NP-Classifier) | [Tool documentation](https://github.com/albertogilf/nextflow_NP-Classifier) | ---  |


### MS2LDA
| [Link](https://gnps2.org/workflowinput?workflowname=ms2lda_nextflow_workflow) | [Source Code](https://github.com/glasgowcompbio/pySubstructures) | [Tool documentation](https://ms2lda.org/user_guide/) | [Citation](https://academic.oup.com/bioinformatics/article/34/2/317/4158166)  |


### ChemWalker
| [Link](https://gnps2.org/workflowinput?workflowname=chemwalker_nextflow_workflow) | [Source Code](https://github.com/computational-chemical-biology/ChemWalker/tree/master) | [Tool documentation](https://github.com/computational-chemical-biology/ChemWalker/tree/master) | [Citation](https://academic.oup.com/bioinformatics/article/39/3/btad078/7067745?login=true)  |
