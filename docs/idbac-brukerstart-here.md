### If you are starting with raw Bruker data, use this flow chart to prepare your files for analysis or deposition. 
*Click on a step for links to the required tools/pages.*


<div align="center">
    
```mermaid
flowchart TD
    A[Starting with raw Bruker data] --> B[Convert raw protein data to mzML via msConvert]
    B --> C[Download and fill out a MALDI TOF plate map]
    C --> D[Upload converted mzML files and plate map to GNPS2]
    D --> E[Run the IDBac_split_MALDI workflow]
    E --> F[Contribute to the IDBac database]
    F --> G[Proceed to the 'Contribute to the database' documentation]
    E --> H[Run an analysis workflow]
    H --> I[Proceed to the analysis documentation]
    
    click B href "https://proteowizard.sourceforge.io/"
    click C href "https://docs.google.com/spreadsheets/d/1ihFy6lQyJtWy9fp46ahMPWk7xLp2tJ3q/edit?usp=sharing&ouid=102573514213912402103&rtpof=true&sd=true"
    click D href "https://gnps2.org/homepage"
    click E href "https://gnps2.org/workflowinput?workflowname=idbac_split_maldi_workflow"
    click G href "https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacdepositions/"
    click I href "https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacsumbmitdata/"

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
  <summary>Navigating MSConvert</summary>
<p>Use the following images to convert raw Bruker data to mzML using MSConvert</p>

    
  <ul>
<img width="1054" alt="MSConvertEDITED" src="https://github.com/user-attachments/assets/a4aafff0-1740-4bd7-8741-83e82af079a6">
<img width="1054" alt="msconvert1" src="https://github.com/user-attachments/assets/cad440c8-917a-463f-a247-bc9f12ac3236">
<img width="1066" alt="msconvert2" src="https://github.com/user-attachments/assets/91edf847-5647-4c89-bddd-154cde86a91c">
 </ul>
</details>

<details>
  <summary>Uploading files to the GNPS2 File Browser</summary>
  <ul>
<img width="FileBrowser1" src="https://github.com/user-attachments/assets/61c1f7ec-aee6-4720-8922-249627ab78bf">
<img width="FileBrowser2" src="https://github.com/user-attachments/assets/d6ffe324-b43d-41c6-9765-2ec681985438">



 </ul>
</details>

<details>
  <summary>Accessing your converted files from the split_MALDI workflow</summary><br>
<p>Download the converted and re-named files to your desktop (allowing for manual upload into a File Browser folder)</p>
  <ul> 
<img width="1054" alt="Download1" src="https://github.com/user-attachments/assets/0e007833-e122-4003-a77e-05db076f1c75">
<img width="1054" alt="UPDATED DOWNLOAD" src="https://github.com/user-attachments/assets/6b45ca81-aa5c-4332-9558-a25bfaee7406">

</details>
 </ul>




 




