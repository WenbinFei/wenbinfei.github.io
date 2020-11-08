---
layout: page
title: Network analysis of heat transfer in granular materials
modified: 
excerpt: " "
comments: false
share: false
image:
  feature: 
  credit: 
  creditlink: 
---

- **Fei W, Narsilio GA, van der Linden JH, Disfani MM. Network analysis of heat transfer in sphere packings. Powder Technology 2020, 362:790-804, [do](https://doi.org/10.1016/j.powtec.2019.11.123).**
- **Fei W, Narsilio GA. Network analysis of heat transfer in sands. Computers and Geotechnics 2020, 127:103773, [doi](:https://doi.org/10.1016/j.compgeo.2020.103773).**

### Network construction
A network is a collection of nodes that are linked by edges. Different networks can be constructed and the meanings of nodes and edges change along with the type of the network. In a contact network, each node indicates a particle and an edge connects two nodes when two particles are in contact. Thermal networks are extensions of the contact networks that also consider near-contacts as edges (Fig. 1)

<figure align="center"> 
<img src="/images/network-construction.png" width='100%'/><br>
</figure> 

*Fig.1 Procedures to construct a contact network and a thermal network. Contact edges are in red, near-contact edges are in blue.*

### Complex network theory
- Centrality indicates the node position and the “significance” of a node in the network, with varying types of centrality defining this significance in distinct ways. Five metrics can be used to measure centrality.
	- The degree of a node is measured as the number of edges linked to a node.
	- Closeness centrality is a measure of the distance of a node to all others.
	- Betweenness centrality characterises the importance of a node or an edge as the bridge between other nodes or edges in a network.
	- Eigenvector centrality considers the contribution of nodes to the connectivity of the whole network and indicates the node which has wide-reaching influence in a network.

- Network scale is a measure indicating the average distance of one node from another in a network.
- A cycle in a network is a loop of edges that starts and ends at the same node. An l-cycle is a cycle containing l edges. 3-cycle in contact network can hint the rigidity of granular materials.
- Clustering implies how integrated or fractured the overall network system is.

<figure align="center"> 
<img src="/images/network-features.png" width='100%'/><br>
</figure> 

*Fig.2 Example of the same contact network and its different centrality values for nodes: (a) Degree, (b) Closeness centrality, (c) Betweenness centrality and (d) Eigenvector centrality. Each definition of centrality highlights different significances of centrality at nodes. The colour shows the value of each feature, red means high value while blue represents low value.*

### Complex network feature in granular materials

<figure align="center"> 
<img src="/images/network-features-visulisation.png" width='100%'/><br>
</figure> 

*Fig.3 Networks of the poly-disperse sample with porosity 0.246: (a) Contact network, (b) Thermal network. The colour at nodes represents the node weighted closeness centrality while the colour at edges represents the type of edge (red edges represent particle contacts while the blue edges represent near-contacts). The node size is scaled by particle radius.*

### Advantage of complex network features

Network features can resolve the unavailability of meso-scale characteristics of granular materials. Additionally, more new features can be achieved after weighting contact network by contact area or weighting thermal networks by thermal conductance. The new features have the merit of capturing more information: both the particle connectivity and contact quality, two essential properties to heat transfer. Therefore, it has stronger correlation with effective thermal conductivity of granular materials.

<figure align="center"> 
<img src="/images/network-features-thermal-conductivity.png" width='100%'/><br>
</figure> 

*Fig.4 The relationship between weighted degree from contact network and effective thermal conductivity (ETC) is stronger than that between porosity and ETC*
