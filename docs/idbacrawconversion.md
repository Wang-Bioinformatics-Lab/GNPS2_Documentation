# 1) Convert raw Bruker data to mzML via MSConvert.
  
### *Open MSConvert and proceed to the following steps.*

i) Select your Bruker FID file(s) by clicking 'Browse'.

ii) Click 'Add' to submit your file to the conversion cue.

iii) Select where you would like your file to be saved under "Output Directory".

iv) Ensure mzML is selected under 'Options/Output format'.

v) When the previous steps are completed, click 'Start'.

vi) The output of this conversion will be a single autoexecute mzML for the entire plate or single mzML files for each well. These files will be re-named and replicates will be merged within the "Idbac_split_maldi_workflow" section below.

<img width="1054" alt="autoexex" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/54cb4f20-2283-431f-b698-6757f2d3125f">

<img width="1066" alt="Manualex" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/e3798a46-19ce-4f99-979d-febc9f9f8338">

![image](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/98c67e40-dcab-4d12-9178-f58432b9665d)

# 2) Upload mzML files to GNPS2.org

i) Select "File Browser" found on the GNPS2.org homepage.

ii) Create a new folder and upload your converted files.

![image](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/d7db9757-c14d-4a8f-97a3-8a61dd90ddf3)

![image](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/ef017f85-3315-4ce1-8c24-cb1bf948c41b)

# 3) Split/ re-name autoexecute file

*For Autoexecute mzML: This workflow will split your autoexecute data into individually labeled mzML files based on your plate map and well positions.*


*For manual collection mzML: This workflow will re-name your mzML files based on your plate map and well positions*

i) Open the [idbac_split_maldi workflow](https://gnps2.org/workflowinput?workflowname=idbac_split_maldi_workflow)

ii) Select your autoExecute mzML and plate map from the drop down menu.

iii) Submit workflow.

![image](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/318e354a-8159-43f7-98df-e915c3d00d72)

## <ins>4) Choose what you would like to do next:<ins>

   a) **IDBac Analysis:** Analyze spectra within your dataset indepedently, or compare against the IDBac protein database (See "Analysis options" below).

   b) **IDBac Protein Database Deposition:** Deposit metadata and spectra of genetically verified isolates into the IDBac database.

 <img width="992" alt="Picture4" src="https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/438b762a-07d1-4dee-bd19-e7dd231bfb92">




