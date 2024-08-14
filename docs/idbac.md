# IDBac Database Submission and Analysis  

[Protein Metadata Sheet](https://docs.google.com/spreadsheets/d/1yKsZ2FEw8-cWufvY8l31Ju8NTKujmEtb/edit?usp=sharing&ouid=102573514213912402103&rtpof=true&sd=true)

### *IDBac workflows require a mzML file format. For guidance on how to convert raw data or mzXML to mzML, see the tabs to the left. 
 
 ## <ins>1) Upload mzML files to GNPS2.org
 
   i) Select "File Browser" found on the [GNPS2.org](https://gnps2.org/homepage) homepage.<ins>
   
   ii) Create a new folder and upload your mzmL files, plate map and metadata sheet.
 

<img width="1096" alt="FileBrowserEx1" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/1bbcc5be-f17f-469b-81f0-864aed4022c6">

<img width="1119" alt="SourceExamples" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/25a5cc68-051f-43ce-bc6c-a9fe08bf1aba">



## <ins>3) Split re-name autoexecute file

This workflow will split your autoexecute data into individually labeled mzML files based on your plate map and well positions. 

   i) Open the [idbac_split_maldi workflow](https://gnps2.org/workflowinput?workflowname=idbac_split_maldi_workflow)
      
   ii) Select your autoExecute mzML and plate map from the drop down menu.
      
   iii) Submit workflow.

<img width="991" alt="Finalsplitmaldi" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/f40702df-7337-47dc-92d0-fbef29742eee">


## <ins>4) Choose what you would like to do next:<ins>

   a) **IDBac Analysis:** Analyze spectra within your dataset indepedently, or compare against the IDBac protein database (See "Analysis options" below).

   b) **IDBac Protein Database Deposition:** Deposit metadata and spectra of genetically verified isolates into the IDBac database.

 <img width="992" alt="Picture4" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/438b762a-07d1-4dee-bd19-e7dd231bfb92">


## <ins> a) IDBac Analysis

**<ins>Submit workflow:** Select [idbac_analysis_workflow](https://gnps2.org/workflowinput?workflowname=idbac_analysis_workflow) and reference the following image for submission instructions.

*If you do not submit metadata during this step, you will have fewer analysis options.

<img width="994" alt="Analysis submission2" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/f99ab189-0686-4415-b848-bf4da0d8fd7e">


**<ins>Analysis options:** Once the idbac_analysis_workflow is complete, you have the ability to analyze your data through:

   i) Vizualize protein dendrogram: View a dendrogram of your isolates (excluding database seeds). 
   
   ii) Visualize with Metadata: If you selected a metadata column to display, it will appear within this protein dendrogram. If you do not select a metadata column to display, a 500 server error will display on-screen should you choose this analysis.
  
   iii) Spectra summary: This option allows you to compare mirror plots of your spectra.

   iv) Dendrogram similarity: You may view similarity scores between your isolates based on the similarity metric you chose in the analysis workflow submission.
   
   v) Database Search Summary: Here you query protein spectra of your unknown isolate against our database of characterized bacterial strains (based on similairty scores).
   

<img width="986" alt="Finalanalysis" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/378353bc-0ee9-411b-a5c4-83bd6f286826">


## b) IDBac Database Deposition 

**<ins>Submit workflow:** Select [idbacdeposition_workflow](https://gnps2.org/workflowinput?workflowname=idbacdeposition_workflow) and reference the following image for deposition instructions.

<img width="993" alt="Databasesubmissionfinal" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/514765f1-560e-4dad-8307-c899993b907f">

**<ins>View Database**

To view your deposition, visit the [IDBac Knowledgebase](https://idbac-kb.gnps2.org/).


## <ins>3) Analysis options: 

Once the idbac_analysis_workflow is complete, you have the ability to analyze your data through:

  __i) Interactive IDBac Analysis:__ Choose parameters and visually analyze your dataset. See section below for more details.
   
  __ii) Database Search Summary:__ Compare protein spectra of your unknown isolate against our database of characterized bacterial strains and obtain similarity scores.
   

![1](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/e940dc4c-02f3-4d9f-b230-0b4cb89e9e05)


## i) Interactive IDBac Analysis
*See images below for more detail*

__a)__ If you did not include a metadata spreadsheet during the workflow submission, you may upload the file here.

__b)__ Choose your preferred parameters for dendrogram visualization.

__c)__ Select how database hits will be displayed in the dendrogram. 

__d)__ If you would like to remove isolates from the dendrogram, you may do so here. 

__e)__ You can choose a dendrogram cut-height and/or display dendrogram distance values for each isolate. 

__f)__ Your dendrogram will be displayed according to the parameters set above. Note: Database strains will be labeled as 'DB'.

__g)__ Visualize a single spectrum or compare two spectra via a mirror plot. 

__h)__ URL link to easily share this analysis page.

![a1](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/85c787fc-2ec6-4cae-af4e-c58bf4903da9)

![a2](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/8d60bbe3-69f2-44c1-9fca-4428d1212b56)

![a3](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/5dc59355-a75b-4008-9b73-dbc9e3c6f418)

![a4](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/81629d5d-bf51-41d8-9998-880b681c0974)

## ii) Database Search Summary

![dbsearch](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/18d5e695-35c6-422f-847b-3c33699afb8e)











