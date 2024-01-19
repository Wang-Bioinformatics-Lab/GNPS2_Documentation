## ChemicalStructureWebService
<details>
<summary>Web Server for Chemical Structure pictures as well as other chemical structure things</summary>

### Web API Endpoints

Full resolution of all structural information conversion

```https://structure.gnps2.org/convert?smiles=CCO```

InChI Conversion

```https://structure.gnps2.org/inchi?smiles=CN1C=NC2=C1C(=O)N(C(=O)N2C)C```

InChIKey Conversion

```https://structure.gnps2.org/inchikey?smiles=CN1C=NC2=C1C(=O)N(C(=O)N2C)C```

Smiles Conversion

```https://structure.gnps2.org/inchikey?smiles=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3```

Mol Conversion

```https://structure.gnps2.org/mol?smiles=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3```

ClassyFire

```https://structure.gnps2.org/classyfire?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3```

Formula

```https://structure.gnps2.org/formula?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3```

Structure Mass

```https://structure.gnps2.org/structuremass?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3```
```https://structure.gnps2.org/structuremass?formula=C8H10N4O2```

Structure Fingerprint

```https://structure.gnps2.org/structurefingerprint?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3```

Image Creation

```https://structure.gnps2.org/structureimg?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3```

Structure Similarity

```https://structure.gnps2.org/structuresimilarity?inchi1=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3&smiles2=CN1C=NC2=C1C(=O)N(C(=O)N2C)C```
</details>

## Fast Search
<details>
<summary>Rapidly search pre-made libraries GNPS and MassIVE spectral data.</summary>
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

</details>

## Public Dataset Files
<details>
<summary>Access spectral data by USI or SpectrumID</summary>  
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
</details>
