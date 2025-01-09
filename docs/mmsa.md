## Multiple Mass Spectral Alignment
MMSA is an interactive web-based tool that improves the interpretability of molecular networks by visualizing the detailed spectral alignment information of a molecular network component. It identifies shared fragment peaks (peak sets) across spectra, providing insights into the structural relationships within molecular families. MMSA’s interface allows users to explore and analyze the global alignment of molecular networks, enabling deeper insights into molecular relationships.

Access the tool [here](https://multiplealignment.gnps2.org/setscreation/).
If you have an existing peak sets file, you can directly access the visualization tool [here](https://multiplealignment.gnps2.org/spectraalignment). 

### MMSA Web Interface Input Options

#### Task id and component number
Enter a GNPS2 task ID and component number to visualize alignments for a specific molecular network.

#### USI input
Input line-separated Universal Spectrum Identifiers (USIs) to define a custom molecular network. 

### MMSA Output

#### Visualizing the Spectral Alignment
After providing input, click the “Process and Save JSON” button to calculate alignments. Once processed, click “View Alignment” to display the interactive visualization.

#### Customizations
Users can specify the x-axis and y-axis limits to zoom in and focus on peaks of interest. The order of spectra displayed in the alignment can also be customized based on spectrum scan numbers. Note that changing the order does not affect the calculated spectral alignment.

#### Peak Sets
The default display is the top 3 largest peak sets highlighted in red, green, and blue.

#### Highlighted Peak Sets
Click on any peak to view the peaks that are in its set and the alignment information across spectra, including scan number, peak index, precursor m/z, peak m/z, and intensity.

### Source Code 
View the source code [here](https://github.com/Wang-Bioinformatics-Lab/NetworkFamily_MultipleAlignment_Website). 