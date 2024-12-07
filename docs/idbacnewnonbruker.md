### 🚧 Work In Progress
This page is under construction, thanks for your patience!


### If you are starting with raw non-Bruker data, use this flow chart to prepare your files for analysis or deposition. 
*Click on a step for links to the required tools/pages.*


<div align="center">
    
```mermaid
flowchart TD
    A[Starting with raw non-Bruker data] --> B[Convert raw data to mzML via msConvert]
    B --> C[Download and fill out an msConvert_File_Merger spreadsheet]
    C --> D[Upload converted mzML files and completed msConvert_File_Merger spreadsheet to File Browser]
    D --> E[Merge replicate files using the msConvert_File_Merger workflow]
    E --> F[Contribute to the IDBac database]
    F --> G[Proceed to the 'Contribute to the database' documentation]
    E --> H[Run an analysis workflow]
    H --> I[Proceed to the analysis documentation]
    
    click B href "https://proteowizard.sourceforge.io/"
    click C href "https://docs.google.com/spreadsheets/d/1o5K4SavD14K-LqhSeWkt4h20MTrAUpkXsaFRYqNdRvY/edit?gid=508446939#gid=508446939"
    click D href "https://gnps2.org/homepage"
    click E href "https://gnps2.org/workflowinput?workflowname=msConvert_File_Merger"
    click G href "https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacdepositions/"
    click I href "https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacsumbmitdata/](https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacsumbmitdata/"

 %% Styling
    style A fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style B fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style C fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style D fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style E fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style F fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style G fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style H fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style I fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px 

%% Link Styling
    linkStyle 0 stroke:#ffcc33,stroke-width:3px
    linkStyle 1 stroke:#ffcc33,stroke-width:3px
    linkStyle 2 stroke:#ffcc33,stroke-width:3px
    linkStyle 3 stroke:#ffcc33,stroke-width:3px
    linkStyle 4 stroke:#ffcc33,stroke-width:3px
    linkStyle 5 stroke:#ffcc33,stroke-width:3px
    linkStyle 6 stroke:#ffcc33,stroke-width:3px
    linkStyle 7 stroke:#ffcc33,stroke-width:3px
  
   
    

```
</div>

### More Resources
<details>
  <summary>Instructions for filling out the msConvert_File_Merger spreadsheet</summary>


i) Insert the current filenames for your individual mzML files into the 'input_filename' column. It is important to keep the '.mzml' tag on the end of the filename in this column. Take care to make sure the filenames in the spreadsheet under 'input_filename' match the filenames in your data folder.

ii) Type a new filename for replicate spectra you would like to combine into a single mzml file. You do NOT need to include the '.mzml' tag in this column. Make sure the 'output_filename' is identical for all replicate spectra you want to be merged. Otherwise the workflow will write files with different 'output_filename' entries as separate mzML files. 
    
  <ul>
<img width="nonBruker1" src="https://github.com/user-attachments/assets/0161167f-bc69-437d-bac2-6c5c909b0be3">

 </ul>
</details>

<details>
  <summary>Uploading files to the GNPS2 File Browser</summary>

    
  <ul> 
<img width="FileBrowser1" src="https://github.com/user-attachments/assets/8b0fc3af-089b-4686-95f9-1135d0cf4c51">
<img width="1054" alt="nonBruker2" src="https://github.com/user-attachments/assets/928ba3c5-f566-45a4-ace4-940d38212de6">
 </ul>
</details>

<details>
  <summary>Navigating the msConvert_File_Merger workflow</summary>

    
<p>This workflow will combine spectra from separate spots that correspond to the same bacterial strain (i.e. replicate spots). The output is a single mzML file (per strain) that contains the replicate spectra as separate scans.</p>


i) Open the msConvert_File_Merger workflow.


ii) Select your mzML files and your input/output spreadsheet from the dropdown menus.


iii) Select mzML or mzXML as your output data format.


iV) Submit workflow.


<img width="msConvert_File_Merger workflow" src="https://github.com/user-attachments/assets/47689134-5d68-423c-8d5a-cde0d62f15cd">
    
  <ul> 




 </ul>
</details>

