## GNPS2

TODO

## ChemicalStructureWebService
Web Server for Chemical Structure pictures as well as other chemical structure things

### Web API Endpoints

Full resolution of all structural information conversion

```
https://structure.gnps2.org/convert?smiles=CCO
```

InChI Conversion

```
https://structure.gnps2.org/inchi?smiles=CN1C=NC2=C1C(=O)N(C(=O)N2C)C
```

InChIKey Conversion

```
https://structure.gnps2.org/inchikey?smiles=CN1C=NC2=C1C(=O)N(C(=O)N2C)C
```

Smiles Conversion

```
https://structure.gnps2.org/inchikey?smiles=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3
```

Mol Conversion

```
https://structure.gnps2.org/mol?smiles=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3
```

ClassyFire

```
https://structure.gnps2.org/classyfire?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3
```

Formula

```
https://structure.gnps2.org/formula?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3
```

Structure Mass

```
https://structure.gnps2.org/structuremass?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3
```

```
https://structure.gnps2.org/structuremass?formula=C8H10N4O2
```

Adduct Masses

```
https://structure.gnps2.org/adductcalc?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3
```

Structure Fingerprint

```
https://structure.gnps2.org/structurefingerprint?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3
```

Structure Drawing

```
https://structure.gnps2.org/structureimg?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3
```

Structure Similarity

```
https://structure.gnps2.org/structuresimilarity?inchi1=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3&smiles2=CN1C=NC2=C1C(=O)N(C(=O)N2C)C
```

### Structure Natural Product Classifier (NP Classifier)

If you have Smiles

```
https://npclassifier.gnps2.org/classify?smiles=<smiles string>
```

[Example](https://npclassifier.gnps2.org/classify?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

??? info "Example JSON Output"
    ```
    {
        class_results: [
            "Purine alkaloids"
        ],
        superclass_results: [
            "Pseudoalkaloids"
        ],
        pathway_results: [
            "Alkaloids"
        ],
        isglycoside: false,
        fp1: [
            0,
            0
            ...
        ],
        fp2: [
            0,
            0,
            ...
        ]
    }
    ```

!!! note "NPClassifier" 
    NPClassifier is A Deep Neural Network-Based Structural Classification Tool for Natural Products - check it out [here](https://npclassifier.gnps2.org/). For citation: Kim, Hyun Woo, Mingxun Wang, Christopher A. Leber, Louis-Félix Nothias, Raphael Reher, Kyo Bin Kang, Justin JJ van der Hooft, Pieter C. Dorrestein, William H. Gerwick, and Garrison W. Cottrell. "NPClassifier: A deep neural network-based structural classification tool for natural products." Journal of Natural Products (2020). [https://doi.org/10.1021/acs.jnatprod.1c00399](https://pubs.acs.org/doi/abs/10.1021/acs.jnatprod.1c00399?casa_token=MRiUf8bJSAcAAAAA:2543Xv_7W0c-AyhntroXm62ccn0QL6c8CpxT0U6NnDoj3JpB1T6Wlr5G96Rfucmnoi2yR0XFgbp2Sw). Checkout the tool index for a large scale workflow for batch classification. 




## ReDU Metadata

Getting files for a given metadata category
```
https://redu.gnps2.org/attribute/<attribute>/attributeterm/<term>/files?filters=%5B%5D
```

Getting all terms per attribute
```
https://redu.gnps2.org/attribute/<attribute>/attributeterms?filters=%5B%5D
```

## Fast Search

Rapidly search pre-made libraries GNPS and MassIVE spectral data.

Search by peaks in json format using query_spectrum:
  
```
https://fasst.gnps2.org/search?usi=None&precursor_mz=981.54&charge=1&library=gnpslibrary&query_spectrum={%22n_peaks%22:15,%22peaks%22:[[165.06979370117188,0.38009798526763916],[167.072998046875,1.7413330078125],[179.07260131835938,0.2999509871006012],[180.08079528808594,100.0],[181.08859252929688,2.8455820083618164],[182.09649658203125,23.914995193481445],[192.08079528808594,0.6896359920501709],[193.0886993408203,0.2419929951429367],[208.07569885253906,3.9236950874328613],[210.09129333496094,51.83255386352539],[236.0706024169922,4.025279998779297],[253.09719848632812,21.652437210083008],[254.08120727539062,46.069068908691406],[255.0872039794922,0.3038550019264221],[271.1077880859375,0.7285820245742798]],%22precursor_charge%22:0,%22precursor_mz%22:271.1077}
```

Search by USI:

```
https://fasst.gnps2.org/search?library=gnpslibrary&usi=mzspec:GNPS:GNPS-LIBRARY:accession:CCMSLIB00000001547
```

Parameters:
* usi (mutually exclusive with query spectrum)
* library: The pre-built library index, options are listed on the [Fast Search GUI](https://fasst.gnps2.org/fastsearch/)
* analog: [Yes/No], Defaults to "No"
* cache: [Yes/No], Defaults to "No"
* lower_delta: defaults to 130
* upper_delta: defaults to 200
* pm_tolerance (Da): The tolerance for precursor mass matching in daltons, defaults to 0.05
* fragment_tolerance (Da): The tolerance for matching individual peaks in daltons, defaults to 0.05
* cosine_threshold: The minimum cosine threshold to be included in the results, defaults to 0.7
* query_spectrum (mututally exclusive with USI): A json formatted peak list

## Public Dataset Files
Access spectral data by USI or SpectrumID
Getting all files per dataset

```
https://explorer.gnps2.org/api/datasets/{accession}/files
```

Getting file path per USI

```
https://dashboard.gnps2.org/downloadlink?usi={file usi}
```

Getting spectrum data from Spectrum ID

```
https://external.gnps2.org/gnpsspectrum?SpectrumID={Spectrum ID}
```

JSON Peak List from USI
```
https://fasst.gnps2.org/search?library=gnpslibrary&usi={file usi}
```
JSON Peak List from USI (Example):
```
https://fasst.gnps2.org/search?library=gnpslibrary&usi=mzspec:GNPS:GNPS-LIBRARY:accession:CCMSLIB00000001547
```


## ModiFinder
Some functions of the ModiFinder visualizer module are accessible via APIs. For details on the parameters you can pass to these functions, refer to the [GitHub](https://github.com/Wang-Bioinformatics-Lab/ModiFinder_base) repository or the [documentation](https://wang-bioinformatics-lab.github.io/ModiFinder_base/modifinder/drawing.html#).

### Draw Molecule
```
https://modifinder.gnps2.org/api/visualizer/draw_molecule?{function argument1}={argument1}&{function argument2}={value2}...{function argumentn}={argumentn}.{type}
```
More details on the function arguments and the argument type are available on the [documentation page](https://wang-bioinformatics-lab.github.io/ModiFinder_base/modifinder/drawing.html#modifinder.utilities.visualizer.draw_molecule). The type can be png or svg.

Exampes:
* [https://modifinder.gnps2.org/api/visualizer/draw_molecule?mol=CCO.svg](https://modifinder.gnps2.org/api/visualizer/draw_molecule?mol=CCO.svg)
* [https://modifinder.gnps2.org/api/visualizer/draw_molecule?mol=CCMSLIB00010102097&size=400,400&highlightAtoms=0,1,5.png](https://modifinder.gnps2.org/api/visualizer/draw_molecule?mol=CCMSLIB00010102097&size=400,400&highlightAtoms=0,1,5.png)


### Draw Modification

You can also draw the modification between two molecules
```
https://modifinder.gnps2.org/api/visualizer/draw_modifications?{function argument1}={argument1}&{function argument2}={value2}...{function argumentn}={argumentn}.{type}
```

Example:
* [https://modifinder.gnps2.org/api/visualizer/draw_modifications?mol1=CCMSLIB00010101989&mol2=CCMSLIB00010102097.png](https://modifinder.gnps2.org/api/visualizer/draw_modifications?mol1=CCMSLIB00010101989&mol2=CCMSLIB00010102097.png)

### Draw Spectrum

```
https://modifinder.gnps2.org/api/visualizer/draw_spectrum?{function argument1}={argument1}&{function argument2}={value2}...{function argumentn}={argumentn}.{type}
```
Example:
* [https://modifinder.gnps2.org/api/visualizer/draw_spectrum?spectrum=CCMSLIB00010102097&bar_width=1.png](https://modifinder.gnps2.org/api/visualizer/draw_spectrum?spectrum=CCMSLIB00010102097&bar_width=1.png)

### Draw Alignment
```
https://modifinder.gnps2.org/api/visualizer/draw_alignment?{function argument1}={argument1}&{function argument2}={value2}...{function argumentn}={argumentn}.{type}
```

Example:

* [http://localhost:5003/api/visualizer/draw_alignment?spectrums=[%22CCMSLIB00010118942%22,%22CCMSLIB00010118185%22,%22CCMSLIB00010104042%22]&matches=default&ratio_to_base_peak=0.01&bar_width=1.png](http://localhost:5003/api/visualizer/draw_alignment?spectrums=[%22CCMSLIB00010118942%22,%22CCMSLIB00010118185%22,%22CCMSLIB00010104042%22]&matches=default&ratio_to_base_peak=0.01&bar_width=1.png)
