## Overview of GNPS2 Workflow Development

Here is the template for GNPS2 Workflows, it provides boiler plate for NextFlow and the accompanying yaml files for input and display. There are several distinct steps that we would recommend:

1. Make a new repository for the GNPS2 workflow that uses this [template](https://github.com/Wang-Bioinformatics-Lab/Nextflow_Workflow_Template)
1. Make sure you can run the template by having conda and nextflow installed
1. Run the test with ```make run```
1. Once your workflow is how you like it in nextflow, you can hook everything up with the workflowinput.yaml file to define the input form. The specifics on each thing are below
1. Update the workflow name so it is unique to your workflow in workflowinput.yaml
1. Update the workflow name for results in workflowresults.yaml
1. To deploy to Dev GNPS2 instance, send Ming your preferred username and public ssh key
1. Prep deployment environment
1. Deploy to GNPS2 Dev instance, see below on how to do that

## Defining GNPS2 Workflow Input YAML

For each workflow, there is a yml file called: workflowinput.yaml. It requires the following items:

```
workflowname: classic_networking
workflowdescription: LC - Classical Molecular Networking
workflowlongdescription: Molecular networks ...
workflowversion: "0.1"
workflowfile: workflows.nf
workflowautohide: false
adminonly: true
parameterlist:
```

### Workflow Input Parameters

Text Entry

```
    - displayname: Precursor Ion Tolerance
      paramtype: text
      nf_paramname: precursor_mass_tolerance
      formplaceholder: Enter the Precursor Ion Tolerance
      formvalue: "2.0"
      tooltip: "Lorem Ipsum"
```

Text Area

```
    - displayname: USI Entry
      paramtype: textarea
      nf_paramname: usi_field
      formplaceholder: Enter USIs
      formvalue: ""
      rows: 4
      cols: 50
```

Drop Down List

```
    - displayname: Network Generation Mode
      paramtype: select
      nf_paramname: cosinemode
      formvalue: fast
      options:
        - value: python
          display: python
        - value: fast
          display: fast
      options-from-file: options.csv
      options-from-url:
        url: https://gnps-external.ucsd.edu/gnpslibrary
        value-key: "name"
        display-key: "name"
```

NOTE: For options-from-url, the API expects to return in json format, a list of dictionaries. Each dictionary will have the same keys, and the users can specify the value and display for the keys in the dropdown.

Section Header

```
    - displayname: Advanced Network Options
      paramtype: section
```

File Selector

```
    - displayname: Metadata Path
      paramtype: fileselector
      nf_paramname: metadata_filename
      formplaceholder: Enter the path to metadata
      formvalue: ""
      targettaskfolder: metadata_folder
      optional: true
      selectsinglefile: false
      folderunroll: true
      linkdata: true
```

1. optional means that if nothing is selected, it will default the nextflow argument to NO_FILE
1. selectsinglefile means that it will take the first selected file as the nextflow argument rather than the whole folder
1. folderunroll means that we will file all the leaf files and symlink them into the target folder, false means we will simply link the select file or folder as is
1. linkdata means that any linking will happen, by default on, but can turn off in cases where we simply want to specify files and not actually do anything with it beyond the name.
1. targettaskfolder is the folder where you put the data on the server 

### Workflow Display Parameters

Pure Java Script Client Side Tables

```
-   name: Results
    displayname: Results
    viewname: results
    displaytype: datatable
    parameters:
        filename: library/results.tsv
        error_missingfile: "No File"
        columns:
            -   title: "Visualize"
                data: 
            -   title: "SpecFile"
                data: filename
        columnDefs: '[ {"targets": 0,"data": null,"render": function ( data, type, row, meta ) {
        return `
            <a target="_blank" href="https://metabolomics-usi.gnps2.org/dashinterface/?usi1=mzspec:GNPS2:TASK-${task}-input_file_folder/${row["filename"]}:scan:${row["scan1"]}">View Spectrum</a>
        `;}}]'
```


Serverside Tables (Medium Sized)

```
-   name: Results
    displayname: Results
    viewname: results
    displaytype: datatable_server
    parameters:
        filename: library/results.tsv
        error_missingfile: "No File"
        columns:
            -   title: "Visualize"
                data: 
            -   title: "SpecFile"
                data: filename
        columnDefs: '[ {"targets": 0,"data": null,"render": function ( data, type, row, meta ) {
        return `
            <a target="_blank" href="https://metabolomics-usi.gnps2.org/dashinterface/?usi1=mzspec:GNPS2:TASK-${task}-input_file_folder/${row["filename"]}:scan:${row["scan1"]}">View Spectrum</a>
        `;}}]'
```

Serverside Tables (Large Sized - GB+ Size)

```
-   name: Results
    displayname: Results
    viewname: results
    displaytype: datatable_serverbig
    parameters:
        filename: library/results.tsv
        error_missingfile: "No File"
        columns:
            -   title: "Visualize"
                data: 
            -   title: "SpecFile"
                data: filename
        columnDefs: '[ {"targets": 0,"data": null,"render": function ( data, type, row, meta ) {
        return `
            <img src="https://structure.gnps2.org/structureimg?smiles=${row["smiles"]}"/>
        `;}}]'
```

Linkout

```
-   name: Downstream Analysis - Run Analysis
    displayname: Downstream Analysis - Run Analysis
    viewname: downstreamworkflow
    displaytype: linkout
    parameters:
        baseurl: /workflowinput
        urlparam:
            -   workflowname:reanalysis_workflow
        hashparam:
            -   input_spectra:TASKLOCATION/[task]/input_spectra
            -   description:Downstream from [task] Molecular Networking


-   name: Visualize Heatmap
    displayname: Visualize Heatmap
    viewname: visualizeheatmap
    displaytype: linkout
    parameters:
        baseurl: /taskresult/[task]/file/nf_output/output.html
        urlparam:
            -   attachment:no
```


Here if we want to use the task params in the linkout, simply use the syntax

```[@paramname]```

Download Files

```
-   name: Download PCoA
    displayname: Download PCoA
    viewname: poca
    displaytype: download
    parameters:
        filename: pcoa/pcoa.qzv
```

Section Division

```
-   name: section
    displayname: Summary Views
    viewname: section
    displaytype: section
```

#### Display Widgets

We can have little widgets to render in the table rows. To make them, you overwrite the columnDefs key. Here are a few examples.

Spectrum Resolver Linkouts

```
'[ {"targets": 0,"data": null,"render": function ( data, type, row, meta ) {
        return `
            <a target="_blank" href="https://metabolomics-usi.gnps2.org/dashinterface/?usi1=mzspec:GNPS2:TASK-${task}-input_file_folder/${row["filename"]}:scan:${row["scan1"]}">View Spectrum</a>
        `;}}]'
```

Structure Display

```
'[ {"targets": 0,"data": null,"render": function ( data, type, row, meta ) {
        return `
            <img src="https://structure.gnps2.org/structureimg?smiles=${row["smiles"]}"/>
        `;}}]'
```
