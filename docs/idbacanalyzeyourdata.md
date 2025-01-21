### 🚧 Work In Progress
This page is under construction, thanks for your patience!

### Analyze your data

This flow chart is a guide on how to submit an analysis workflow. <br>

**Click on the flow chart boxes for links to the required tools/pages* <br>
**Protein data analysis can be conducted without a metadata sheet.* <br>
**Small molecule data analysis requires a metadata sheet.*

<div align="center">
    
```mermaid
flowchart TD
    A[Submit your data for analysis] --> B[Download and fill out an analysis metadata sheet]
    B --> C[Upload your metadata and mzML files to the GNPS2 File Browser]
    C --> D[Open the idbac_analysis_workflow]
    D --> E[Select appropriate data for each file selection section]
    E --> F[Select preferred distance metric]
    F --> G[Select preferred database distance threshold]
    G --> H[Submit workflow]
    H --> I[Choose a data analysis option]
    I --> J[Web IDBac Analysis Platform]
    J --> K[Database Search Summary- see tab below]
   
    click B href "https://docs.google.com/spreadsheets/d/1Y7WHrFQR_SYpR_p5u_xL4BQimYorQ3-1PfAfVil3nL0/edit?gid=678327011#gid=678327011"
    click D href "https://gnps2.org/workflowinput?workflowname=idbac_analysis_workflow"
    click J href "https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/idbacanalysisplatform/"
    


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
<p>This page can also be found in the Metadata Excel doc.</p>
  <ul>
<img width="1054" alt="<img width="932" alt="DepositionMetadataInstructions" src="https://github.com/user-attachments/assets/773eb918-2d19-4fe9-b0f4-03a7f1139099">
 </ul>
</details>

<details>
  <summary>Navigating the idbac_analysis_workflow page</summary>
<p>Use the following images to convert raw Bruker data to mzML:</p>
  <ul>
<img width="analysis page1" src="https://github.com/user-attachments/assets/68336857-8647-40d4-a607-cdbdffa9e950">

 </ul>
</details>
