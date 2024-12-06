### 🚧 Work In Progress
This page is under construction, thanks for your patience!

### If you are starting with raw Bruker data, use this flow chart to prepare your files for analysis or deposition. 
#### Click on each step for links to the required tools/pages.


<div align="center">
    
```mermaid
flowchart TD
    A[Starting with raw Bruker data] --> B[Convert raw protein data to mzML via MSConvert]
    B --> C[Download and fill out a MALDI TOF plate map]
    C --> D[Upload converted mzML files and plate map to GNPS2]
    D --> E[Run the IDBac_split_MALDI workflow]
    E --> F[Make a database deposition]
    F --> G[Proceed to the IDBac deposition documentation]
    E --> H[Run an analysis]
    H --> I[Do you have small molecule data you would like to add to the analysis?]
    I --> |No| J[Click 'Downstream Analysis' on the split MALDI page]
    I --> |Yes| K[Complete the steps in this flowchart for your small molecule data]
    K --> L[Proceed to the analysis documentation]
    
    click B href "https://proteowizard.sourceforge.io/"
    click C href "https://docs.google.com/spreadsheets/d/1ihFy6lQyJtWy9fp46ahMPWk7xLp2tJ3q/edit?usp=sharing&ouid=102573514213912402103&rtpof=true&sd=true"
    click D href "https://gnps2.org/homepage"
    click E href "https://gnps2.org/workflowinput?workflowname=idbac_split_maldi_workflow"
    click G href "https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacdepositions/)"
    click L href "https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacsumbmitdata/"

 %% Styling
    style A fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style B fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style C fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style D fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style E fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style F fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style G fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style H fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style I fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style J fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style K fill:#FFFFFF,stroke:#000000,stroke-width:2px
    style L fill:#FFFFFF,stroke:#000000,stroke-width:2px
    
   

%% Link Styling
    linkStyle 0 stroke:#ffcc33,stroke-width:2px
    linkStyle 1 stroke:#ffcc33,stroke-width:2px
    linkStyle 2 stroke:#ffcc33,stroke-width:2px
    linkStyle 3 stroke:#ffcc33,stroke-width:2px
    linkStyle 4 stroke:#ffcc33,stroke-width:2px
    linkStyle 5 stroke:#ffcc33,stroke-width:2px
    linkStyle 6 stroke:#ffcc33,stroke-width:2px
    linkStyle 7 stroke:#ffcc33,stroke-width:2px
    linkStyle 8 stroke:#ffcc33,stroke-width:2px
    linkStyle 9 stroke:#ffcc33,stroke-width:2px
    linkStyle 10 stroke:#ffcc33,stroke-width:2px
    

```
</div>

### More Resources
<details>
  <summary>Navigating MSConvert</summary>
  
  Use the following images to convert raw Bruker data to mzML

<img width="1066" alt="msconvert3" src="https://github.com/user-attachments/assets/478649c9-be10-4460-9d0d-3f4b34171777">
<img width="1054" alt="msconvert1" src="https://github.com/user-attachments/assets/cad440c8-917a-463f-a247-bc9f12ac3236">
<img width="1066" alt="msconvert2" src="https://github.com/user-attachments/assets/91edf847-5647-4c89-bddd-154cde86a91c">

</details>
