# Imitation-on-higher-order-networks
This custom code performs the simulations for the paper: Structure-aware imitation dynamics on higher-order networks. This repository provides Julia code for computing the fixation probabilities of cooperators and defectors on a given higher-order network under different update rules in multiplayer evolutionary games.
## Requirements
The code is written in Julia.
After installing the required Julia packages, the simulation can be run directly by executing the .jl file.
## Higher-order network Structure
The higher-order network is specified by an incidence matrix. [`NetworkStructure_HoMo_ind1_Unweighted.txt`](HoMo-N500/NetworkStructure_HoMo_ind1_Unweighted.txt)
In the incidence matrix: 
Rows represent nodes
Columns represent hyperedges

For example:
If in column 1 the entries in rows 2, 4, and 5 are 1 and all other entries are 0, this indicates that nodes 2, 4, and 5 form a hyperedge of size 3.

