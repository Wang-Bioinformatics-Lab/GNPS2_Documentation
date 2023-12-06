This is the conversion for Agilent.

## MSConvert and GNPS2

One of the key issues with Agilent software converted with MSConvert, is that the MSConvert makes the scans non-sequential. Molecular Networking does not like this, so we have created a workflow in GNPS2 that renumbers the MS scans so that it is sequential. The general process involves this:

1. Convert the Agilent data with MSConvert
1. Upload the data to GNPS2
1. Run the [Agilent Conversion workflow](https://gnps2.org/workflowinput?workflowname=agilent_conversion_workflow)
1. Run the [Classical Molecular Networking workflow](https://gnps2.org/workflowinput?workflowname=classical_networking_workflow) in GNPS2.


## Agilent Software - Qual

We can also do export directly from Agilent software.

TODO: Finish this