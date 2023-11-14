## ChemWalker workflow documentation

Chemwalker is a tool published by R. da Silva lab to annotate features in metabolomic networks by propagating annotations on non-directly connected nodes by using MetFrag. The article is published [here](https://academic.oup.com/bioinformatics/article/39/3/btad078/7067745) and the source code is available in [github](https://github.com/computational-chemical-biology). 

### Input

The fields are presented in the image:
![chemwalker input fields image](./img/workflows/chemwalker/chemwalker_input.png). Bold fields are mandatory

1. task description
Optional, a description of the task to ease the user its identification. 

2. **GNPS2, FBMN, or FBMNv2 task id**

The information from the molecular network is necessary to annotate the nodes (features). For that, chemwalker needs the job id of the [molecular network task](https://gnps2.org/workflowinput?workflowname=feature_based_molecular_networking_workflow). To view the task_id, check the image and the red rectangle: 
![task id location image](./img/workflows/task_id.png). 
The task id can be

3. **Workflow type (GNPS2, FBMN or V2)**
The task id of the molecular netowrking. Be aware that tasks from FBMN or molecular networking v2 depend on the GNPS availability and the GNPS2 depends on the GNPS2 availability. If the GNPS server is down, the chemwalker task will not work for those tasks since it needs to retrieve the data from GNPS. Analogously the GNPS2 depends on GNPS2 availability. 

4. **Component (Molecular family) index** 

The component index of the network to annotate. If the user wants to annotate all networks, a 0 shall be introduced. 
The molecular networking has been performed before. If the user only wants to annotate a specific network and its nodes. If a 0 is introduced, all networks will be annotated. If a component index with no nodes is introduced, the task will fail. 

5. **File selection** 

The database where the annotations will be based. This database will be used later to use the MetFrag software against and annotate and score the molecules. 

To create a user specific database, see [https://ccms-ucsd.github.io/GNPSDocumentation/nap/#structure-database](https://ccms-ucsd.github.io/GNPSDocumentation/nap/#structure-database)


### Output

The different parts of the output are presented in the image:
![chemwalker input fields image](./img/workflows/chemwalker/chemwalker_output.png). 

1. **Log Text area**
Text area with the result of the task. If there is some fail, the log will be written there. If the task failed and you want to contact the support team, please provide the output of this text area along with the job id. 

2. **Full results from the job**
Full results from the job. It can provide information to debug or to users with programming knowledge. 

3. **random walk structures.tsv**
File with the annotations over the nodes in the selected network/s. You can download to see the full fields or visit the online version. For a full analysis the download of the file is recommended.

4. **random walk structures.graphml**

Graphml with the annotations to visualize the nodes in Cytoscape. You can import this datafile and dynamically analyze it there.