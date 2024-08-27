# 1) Convert raw MALDI data to mzML via MSConvert

*For raw data file conversion using msConvert, refer to the [Data Conversion](https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacrawconversion/) tab of the IDBac documentation.
The steps are the same for all vendor file formats.*

# 2) Fill out the 'input_filename' and 'output_filename' in the msConvert_File_Merger spreadsheet

[msConvert_File_Merger spreadsheet](https://docs.google.com/spreadsheets/d/1o5K4SavD14K-LqhSeWkt4h20MTrAUpkXsaFRYqNdRvY/edit?gid=508446939#gid=508446939) 

i) Insert the current filenames for your individual mzML files into the 'input_filename' column. It is important to keep the '.mzml' tag on the end of the filename in this column. Take care to make sure the filenames in the spreadsheet under 'input_filename' match the filenames in your data folder.

ii) Type a new filename for replicate spectra you would like to combine into a single mzml file. You do NOT need to include the '.mzml' tag in this column. Make sure the 'output_filename' is identical for all replicate spectra you want to be merge. Otherwise the workflow will write files with different 'output_filename' entries as separate mzML files. 

![input_output_spreadsheet](https://github.com/user-attachments/assets/4d58ea42-1280-4181-ae01-3fc81637c495)

# 3) Upload mzML files and completed msConvert_File_Merger spreadsheet to GNPS2.org

i) Select "File Browser" found on the [GNPS2.org](https://gnps2.org/homepage) homepage.

ii) Create a new folder and upload your converted files.

iii) Upload your completed msConvert_File_Merger spreadsheet.

![image](https://github.com/Wang-Bioinformatics-Lab/GNPS2_Documentation/assets/140128524/d7db9757-c14d-4a8f-97a3-8a61dd90ddf3)

![Strain_platemap_filebroswer](https://github.com/user-attachments/assets/b769b0c3-aea3-40f0-8063-c42646b6fc78)

# 4) Merge spectra for strain replicates using the mzConvert_File_Merger workflow

*This workflow will combine spectra from separate spots that correspond to the same bacterial strain (i.e. replicate spots). The output is a single mzML file (per strain) that contains the replicate spectra as separate scans.* 

i) Open the [msConvert_File_Merger](https://gnps2.org/workflowinput?workflowname=msConvert_File_Merger) workflow.

ii) Select your mzML files and your input/output spreadsheet from the dropdown menus. 

iii) Select mzML or mzXML as your output data format. 

iV) Submit workflow.

![workflow_page](https://github.com/user-attachments/assets/9f81a237-6f79-4593-b5d4-3c11a1d92180)

# 5) Access your data for download and export

i) Select 'See Output Files' to access the merged mzML files in file broswer.

![data_output](https://github.com/user-attachments/assets/3349a539-c13c-4d1a-a175-12b740c80d7f)
