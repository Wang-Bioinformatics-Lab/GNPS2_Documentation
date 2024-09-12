
Waters LCMS data conversion: an easy workflow to convert Waters raw data to open data formats

Waters LCMS raw data can be converted into open data formats, such as mzML, following a simple workflow with only two main steps: 1) File conversion in DataConnect and 2) Scan renumbering using a GNPS2 workflow.


## File conversion in DataConnect (for Windows only):
   
1. Waters files (.raw) are converted into mzML using DataConnect, available from the Waters MicroApps Website: https://microapps.on-demand.waters.com/home/showmarkdown/data-as-a-product. 

1. Follow instructions for downloading, installation and licensing found in the Release Notes: https://proddocuments.on-demand.waters.com/ReleaseNotes/Waters%20Tyne%20Bridge%20ReleaseNotes.pdf.

1. Once DataConnect is properly installed, open it and click on Queue MassLynx tasks button. 

1. Choose the folder where the RAW files (.raw) are. Select the files on the Available RAWs window (left) and they will be moved to the Selected RAWs window (right), then click next.

1. Select the lock mass compound on the top left box for mass correction. Use the defaults parameters, unless needed otherwise (on defatult Zlib compression, Write index and Centroid data using 2D peak peaking are checked). 

1. Choose your m/z compression size (32 or 64 bit), then click next. Choose your output path folder. Log level default is debug. Click export RAWs.

1. You will be directed to the task queue window. The file conversion will start immediately or will be put into queue.

1. Once the file conversion is complete, check in the output path folder, noting if the file size is around the expected size.

1. Transfer the files into your GNPS2 profile, using ftp or sftp. Instructions for file upload can be found here: https://wang-bioinformatics-lab.github.io/GNPS2_Documentation/fileupload/


## Scan renumbering using a GNPS2 workflow.
To correct the MS1 and MS2 scan numbering in the converted files, run the Agilent Workflow on the GNPS2 website.

1. On GNPS2 website (gnps2.org) launch Agilent conversion workflow.

1. Select files from your folder and submit workflow.

1. Converted files can now be used in downstream analysis on the GNPS2 website or downloaded for other analysis.
