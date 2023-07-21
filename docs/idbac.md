Convert raw autoExecute data (Bruker FID) to mzML via MSConvert. 

 <img width="1120" alt="MSConvert Settings1" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/11c83de8-85b1-4eae-bdfa-b80d2f8fde5f">\
 <img width="1120" alt="Choosing File1" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/75cc9747-28ab-41ce-815c-27dfe259b8a4">
 
Upload your converted mzML file along with a MALDI plate map labeled with your isolate IDs (CSV or XLSX) to "File Browser". 

<img width="1096" alt="FileBrowserEx1" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/1bbcc5be-f17f-469b-81f0-864aed4022c6">

<img width="1119" alt="SourceExamples" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/25a5cc68-051f-43ce-bc6c-a9fe08bf1aba">

Split MALDI Workflow submission (https://gnps2.org/workflowinput?workflowname=split_maldi_workflow): Select your autoExecute mzML and plate map from the drop down menu. The output of this workflow is individual, labeled mzML files based on MALDI well-position. 

<img width="1106" alt="SplitWorkflowfinal" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/028cb5fe-290a-4954-aa5b-d45d63bc2fe8">


IDBac Deposition (https://gnps2.org/workflowinput?workflowname=idbacdeposition_workflow): Upload the mzML files from the previous step with the cooresdponding metadata sheet. Ensure "Dryrun mode" is set to "No". 

Once this workflow is submitted, your data will be deposited into the IDBac Database.

<img width="1102" alt="IDBac Deposition" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/94d89ad9-8f72-466b-b6f1-460866f5ea4a">
<img width="1118" alt="MEtadata3" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/f68d7936-c203-4cfa-a34b-fe5fb3c930b5">

