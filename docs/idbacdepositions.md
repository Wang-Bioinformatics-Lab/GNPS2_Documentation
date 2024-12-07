### IDBac Database Depositions
This flow chart is a guide on how to deposit genetically verified strains in the IDBac protein MS database. 

**Click on a step for links to the required tools/pages.*

**IDBac workflows require a mzML file format. For guidance on how to convert raw data or mzXML to mzML, see the 'Start Here' tabs to the left.*


**All database depositions must have either an accompanying accession number or 16S taxonomy assignment and sequence.*

<div align="center">
    
```mermaid
flowchart TD
    A[Contribute to the IDBac protein MS database] --> B[Do you have a single mzML file per strain?]
    B -->|Yes| C[Download and fill out a deposition metadata sheet]
    B -->|No| D[View the 'Start Here' documentation]
    C --> E[Upload your mzML and metadata files to the GNPS2 File Browser]
    E --> F[Open the IDBac deposition workflow]
    F --> G[Choose a task description and select your metadata and spectra mzML files]
    G --> H[Would you like to QC your spectra before deposition?]
    H --> |Yes| I[Select 'Yes' from the 'Dryrun Mode' dropdown and submit workflow]
    H --> |No| J[Select 'No' from the 'Dryrun Mode' dropdown and submit workflow]
    J --> K[View your deposition on the IDBac database web page]
    I --> L[Reference the 'QC your data' tab below]
   
    
    click C href "https://docs.google.com/spreadsheets/d/1yKsZ2FEw8-cWufvY8l31Ju8NTKujmEtb/edit?usp=sharing&ouid=102573514213912402103&rtpof=true&sd=true"
    click E href "https://gnps2.org/homepage"
    click F href "https://gnps2.org/workflowinput?workflowname=idbacdeposition_workflow"
    click K href "https://idbac.org/database"


 %% Styling
    style A fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:24px
    style B fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style C fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style D fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style E fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style F fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style G fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style H fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style I fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style J fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style K fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px
    style L fill:#FFFFFF,stroke:#000000,stroke-width:2px,font-size:18px 

%% Link Styling
    linkStyle 0 stroke:#ffcc33,stroke-width:3px
    linkStyle 1 stroke:#ffcc33,stroke-width:3px
    linkStyle 2 stroke:#ffcc33,stroke-width:3px
    linkStyle 3 stroke:#ffcc33,stroke-width:3px
    linkStyle 4 stroke:#ffcc33,stroke-width:3px
    linkStyle 5 stroke:#ffcc33,stroke-width:3px
    linkStyle 6 stroke:#ffcc33,stroke-width:3px
    linkStyle 7 stroke:#ffcc33,stroke-width:3px
    linkStyle 8 stroke:#ffcc33,stroke-width:3px
    linkStyle 9 stroke:#ffcc33,stroke-width:3px
    linkStyle 10 stroke:#ffcc33,stroke-width:3px
    
   

```
</div>

### More Resources
<details>
  <summary>QC your Data</summary>
<p>Use the following images to convert raw Bruker data to mzML:</p>
  <ul>
<img width="NewQC1" src="https://github.com/user-attachments/assets/14ab8a17-d87a-49ed-a377-9b403552a917">
<img width="NewQC2" src="https://github.com/user-attachments/assets/49b8d828-f71c-414d-9a8c-eeae68f6474b">
<img width="QC5"src="https://github.com/user-attachments/assets/1c32d15e-eb35-4fa7-987a-f29e9617b391">

 </ul>
</details>

<details>
  <summary>Metadata Instructions</summary>
<p>This page can also be found in the Metadata Excel doc.:</p>
  <ul>
<img width="1054" alt="<img width="932" alt="DepositionMetadataInstructions" src="https://github.com/user-attachments/assets/773eb918-2d19-4fe9-b0f4-03a7f1139099">
 </ul>
</details>
