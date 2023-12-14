# IDBac Analysis

## <ins>IDBac Templates<ins>
[MALDI Plate Map](https://docs.google.com/spreadsheets/d/1ihFy6lQyJtWy9fp46ahMPWk7xLp2tJ3q/edit?usp=sharing&ouid=102573514213912402103&rtpof=true&sd=true)

[Metadata Sheet](https://docs.google.com/spreadsheets/d/1yKsZ2FEw8-cWufvY8l31Ju8NTKujmEtb/edit?usp=sharing&ouid=102573514213912402103&rtpof=true&sd=true)

*IDBac workflows require a mzML file format. For guidance on how to convert raw data or mzXML to mzML, see the tabs to the left.*

## <ins>1) Upload mzML files to GNPS2.org
 
   i) Select "File Browser" found on the [GNPS2.org](https://gnps2.org/homepage) homepage.<ins>
   
   ii) Create a new folder and upload your mzML files, plate map and metadata sheet.
 

<img width="1096" alt="FileBrowserEx1" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/1bbcc5be-f17f-469b-81f0-864aed4022c6">

<img width="1119" alt="SourceExamples" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/25a5cc68-051f-43ce-bc6c-a9fe08bf1aba">


## <ins>2) Submit Analysis workflow: 

Select [idbac_analysis_workflow](https://gnps2.org/workflowinput?workflowname=idbac_analysis_workflow) and reference the following image for submission instructions.

*If you do not submit metadata during this step, you will have fewer analysis options.*

<img width="994" alt="Analysis submission2" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/f99ab189-0686-4415-b848-bf4da0d8fd7e">


## <ins>3) Analysis options: 

Once the idbac_analysis_workflow is complete, you have the ability to analyze your data through:

   ii) Query Spectra Summary: Visualize spectra of each strain you are analyzing. 
   
   ii) Vizualize dendrogram: View a protein dendrogram of your isolates (excluding database seeds). 
   
   iii) Visualize with Metadata: If you selected a metadata column to display, it will appear within this protein dendrogram.

   iv) Dendrogram similarity: You may view mirror plots and similarity scores between your isolates based on the similarity metric you chose in the analysis workflow submission.
   
   v) Database Search Summary: Here you query protein spectra of your unknown isolate against our database of characterized bacterial strains (based on similairty scores).
   

<img width="986" alt="Finalanalysis" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/378353bc-0ee9-411b-a5c4-83bd6f286826">

