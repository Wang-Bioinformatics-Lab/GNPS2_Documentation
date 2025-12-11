## Raw Data

We generally accept two formats mzML and mzXML. These are preferred with some caveats on conversion. 

MGF is accepted but its frowned upon as a raw data format as its not really standardized. Here is an example of what it should look like if you want to be able to use it for analysis

```
BEGIN IONS
TITLE=SCAN=1
PEPMASS=981.54
CHARGE=0
MSLEVEL=2
SEQ=*..*
SCANS=1
289.286377	8068.0
295.545288	22507.0
298.489624	3925.0
317.324951	18742.0
319.655945	8604.0
324.482422	8041.0
325.316284	9738.0
339.789429	16145.0
343.947021	18094.0
347.020508	13981.0
347.913391	6765.0
END IONS
```

NOTE: Make sure your file starts at SCANS=1 and is continguous counting up

## MS/MS spectral libraries

We generally support libraries from GNPS, but we also note that you might want to use your own libraries. To that end you could make your own MGF file as a private library. You do miss out on other niceties within the GNPS2 ecosystem but it can be done. The format example is as follows:

```
BEGIN IONS
TITLE=SOMEUNIQUEID
PEPMASS=981.54
CHARGE=0
MSLEVEL=2
SOURCE_INSTRUMENT=LC-ESI-qTof
SEQ=*..*
IONMODE=Positive
NAME=3-Des-Microcystein_LR M+H
PI=Gerwick
DATACOLLECTOR=Jenia
SMILES=CC(C)CC1NC(=O)C(C)NC(=O)C(=C)N(C)C(=O)CCC(NC(=O)C(C)C(NC(=O)C(CCCNC(N)=N)NC(=O)C(C)C(NC1=O)C(O)=O)\C=C\C(\C)=C\C(C)C(O)Cc1ccccc1)C(O)=O
INCHI=N/A
PUBMED=N/A
SUBMITUSER=mwang87
SPECTRUMID=SOMEUNIQUEID
SCANS=1
289.286377	8068.0
295.545288	22507.0
298.489624	3925.0
317.324951	18742.0
319.655945	8604.0
324.482422	8041.0
325.316284	9738.0
339.789429	16145.0
343.947021	18094.0
347.020508	13981.0
347.913391	6765.0
END IONS
```
