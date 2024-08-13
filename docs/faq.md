## Molecular Networking

**Q: My molecule of interest is not appearing in my classical molecular networking. What should I do?**

**A:**

1. **Ensure Inclusion:** First, make sure that your molecule is included in the network and not filtered out by the minimum cluster size setting (the default is 2).
2. **Check for Neighbors:** Next, check if your molecule has any neighboring connections in the network. 
3. **Examine Singletons:** To be thorough, examine the network including singletons.

**Q: How to show the singletons in a network?**

**A:**

At the classical_networking_workflow or feature_based_molecular_networking_workflow task result page, click "Visualize Full Network  w/ Singletons in Browser" in the "Network Visualizations" section.


**Q: I have a ton of data to analyze at GNPS2 but the File Uploader is slow, how do I get my data over there?**

**A:**

GNPS2 has an FTP/SFTP upload portal that is meant for close collaborators to be able to upload a significant amount of data. Otherwise, since GNPS2 does not have the ability to store massive amounts of data for the broader community, we recommend deposition of the data at a public repository such as MassIVE in order to do analysis of such data at GNPS2. 

## Feature-based Molecular Networking

**Q: How do I find the Box Plot of a node?**

**A:**

On the FBMN result page, click "Cluster Summary" and then search for the scan number you are interested in the Cluster column, and then click "View Box Plot". In the Plot Configuration section, you can specify the Metadata Column and then select the groups to be displayed.
