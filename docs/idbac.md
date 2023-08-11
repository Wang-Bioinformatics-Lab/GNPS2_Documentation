1) Convert raw autoExecute data to mzML via MSConvert.
   
   a) Select browse to  your Bruker FID file by clicking 'Browse'
   
   b) Click 'Add' to submit your file to the conversion cue
   
   c) Select where you would like your file to be saved under "Output Directory"
   
   d) Ensure mzML is selected under 'Options/Output format'
   
   e) When the previous steps are completed, click 'Start'

<img width="938" alt="Picture1" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/ce5975a1-4177-4abe-b3da-fddf437f775d">

<img width="948" alt="Picture2" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/3f05f184-1d17-4d4e-80c8-cd4e92477fcd">

 
2) Upload your converted mzML file along with a MALDI plate map labeled with your isolate IDs (CSV or XLSX) to "File Browser" found on the GNPS2.org homepage. 

<img width="1096" alt="FileBrowserEx1" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/1bbcc5be-f17f-469b-81f0-864aed4022c6">

<img width="1119" alt="SourceExamples" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/25a5cc68-051f-43ce-bc6c-a9fe08bf1aba">


3) IDBac_split_MALDI Workflow submission (https://gnps2.org/workflowinput?workflowname=idbac_split_maldi_workflow): Select your autoExecute mzML and plate map from the drop down menu. The output of this workflow is individual, labeled mzML files based on MALDI well-position. 

<img width="995" alt="Picture3" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/5566327a-12a6-4c65-a280-a645de45a5a5">

4) Once this workflow is completed, you will be provided with two options:
   <img width="992" alt="Picture4" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/438b762a-07d1-4dee-bd19-e7dd231bfb92">

   a) IDBac Analyisis: Analyze spectra within your dataset indepedently, or by comparing against the IDBac database (See below for full analysis options).
   <img width="994" alt="Analysis submission2" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/f99ab189-0686-4415-b848-bf4da0d8fd7e">
   
   b) IDBac Database Deposition: Deposit your spectra and metadata into the IDBac database
<img width="993" alt="Databasesubmissionfinal" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/514765f1-560e-4dad-8307-c899993b907f">




IDBac Analysis Options: Within this workflow you have the ability to analyze your data through:

<img width="992" alt="Picture5" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/5c514131-2f8f-4e32-b351-9edc33e2e467">

   a) Vizualize dendrogram: View dendrogram of your data (excluding database seeds).
   
   b) Visualize with Metadata: If you selected a metadata colum to display, it will appear within the dendrogram here. 
      

   c) Spectra summary: This option allows you to compare mirror plots of your spectra.

   d) Dendrogram similarity: You may view similarity scores between your isolates based onthe similarity metric you chose in the analysis workflow submission.       

   e) Database Search Summary: Here you can identify which database seeds that your 
      isolates matched with, based on similairty scores.

















