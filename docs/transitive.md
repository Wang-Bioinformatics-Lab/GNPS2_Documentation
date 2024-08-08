## Transitive Network Topology

Checkout the workflow [here](https://gnps2.org/workflowinput?workflowname=Transitive_alignment_workflow). 

You can also use this after any molecular networking job, either classical or FBMN. 

Citation - In Press

### Network Topology Parameters

#### Transitive Param - Min Clique Cosine
The score threshold to control the edge score within a CAST clique.

#### Transitive Param - Min Transitive Alignment Score
The score threshold for adding a transitive alignment edge back to the network.

#### MST Filter Option
Filter option for each compound after constructing the MN (This is only for better visualization layout). Available options:
- **Pure MST**: Only apply MST on the MN.
- **Greedy MST**: After applying MST, greedily add back high score edges for higher average edge score.
- **Hybrid MST**: Using the original edges first, if unable to create MST, then use the transitive alignment edges to finish the MST.

### Induced Network Parameters

#### Induced Network Param - Option
- **Intersection the Transitive and MAX Hops**: Using this method, if and only if the nodes in the original network are within the max hops of the source node and also the transitive alignment score is above the setting threshold (**Induced Network Param - Min Transitive Alignment Score**) will be in the induced network results.
- **Union the Transitive and Max Hops**: This method will first do all the transitive alignment from the source node to all the other reachable nodes, and then add back the transitive alignment edge above the threshold (**Induced Network Param - Min Transitive Alignment Score**) to the original network. Afterward, select the node within the max hops from the source node or the edge score above the threshold (**Induced Network Param - Min Transitive Alignment Score**) to the results.

#### Induced Network Param - Source Node
The source node to start the induced network.

#### Induced Network Param - Max Hops
Maximum hops from the source node to the target node.

#### Induced Network Param - Min Transitive Alignment Score
The transitive alignment score threshold.

#### Induced Network Param - MST Filter Option
Filter option for the induced network after constructing (This is only for better visualization layout). Available options:
- **Pure MST**: Only apply MST on the MN.
- **Greedy MST**: After applying MST, greedily add back high score edges for higher average edge score.
- **Hybrid MST**: Using the original edges first, if unable to create MST, then use the transitive alignment edges to finish the MST.
