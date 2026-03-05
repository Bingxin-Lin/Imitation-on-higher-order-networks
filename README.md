# Imitation-on-higher-order-networks
This custom code performs the simulations for the paper: Structure-aware imitation dynamics on higher-order networks. This repository provides Julia code for computing the fixation probabilities of cooperators and defectors on a given higher-order network under different update rules in multiplayer games.
## Requirements
The code is written in Julia.
After installing the required Julia packages, the simulation can be run directly by executing the .jl file.
## Higher-order network structures
The higher-order network is specified by an incidence matrix. For example: 
```bash
HoMo-N500/NetworkStructure_HoMo_ind1_Unweighted.txt
```
In the incidence matrix, rows represent nodes and columns represent hyperedges. For example, if in column 1 the entries in rows 2, 4, and 5 are 1 and all other entries are 0, this indicates that nodes 2, 4, and 5 form a hyperedge of size 3.

## Multiplayer games
The code currently includes three multiplayer games studied in the main paper: Linear Public Goods Game (LPGG), Multiplayer Snowdrift Game (MSG), and the Threshold Public Goods Game (TPGG).

## Imitation-based update rules
The update rule is determined by two parameters:

$s$ (number of selected hyperedges)

$q$ (number of social peers selected from each selected hyperedge)

These parameters can be freely specified in the input settings.

## Output
The results are written to a text file. For example:

```bash
HoMo-N500/ConditionalFixationProb_HoMo_ind1_w0.01.txt
```

The file structure is as follows: First 5 rows: fixation probabilities of cooperators; Last 5 rows: fixation probabilities of defectors.

For each row: Column 1: value of the game parameter $r$ (e.g., $r_1$ in the LPGG); Column 2: fixation probability of the corresponding strategy at that parameter value.

## Parallel Computation
Since the simulations require a large number of repetitions, the code supports multi-core parallel computation. You can adjust the variable:

```bash
numLogicCoresUsed
```

to specify how many CPU cores are used, which can significantly accelerate the simulation.
