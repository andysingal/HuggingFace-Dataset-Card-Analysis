---
license: mit
task_categories:
- graph-ml
---

# Dataset Card for AQSOL

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
  - [Supported Tasks and Leaderboards](#supported-tasks-and-leaderboards)
- [External Use](#external-use)
  - [PyGeometric](#pygeometric)
- [Dataset Structure](#dataset-structure)
  - [Data Properties](#data-properties)
  - [Data Fields](#data-fields)
  - [Data Splits](#data-splits)
- [Additional Information](#additional-information)
  - [Licensing Information](#licensing-information)
  - [Citation Information](#citation-information)
  - [Contributions](#contributions)

## Dataset Description
- **[Homepage](https://github.com/graphdeeplearning/benchmarking-gnns)**
- **Paper:**:  (see citation)


### Dataset Summary
The AQSOL dataset comes "from the Benchmarking Graph Neural Networks paper based on AqSolDB, a standardized database of 9,982 molecular graphs with their aqueous solubility values, collected from 9 different data sources" (PyGeometric doc).

### Supported Tasks and Leaderboards
`AQSOL` should be used for graph regression, on aqueous solubility. 

## External Use
### PyGeometric
To load in PyGeometric, do the following:

```python
from datasets import load_dataset

from torch_geometric.data import Data
from torch_geometric.loader import DataLoader

dataset_hf = load_dataset("graphs-datasets/<mydataset>")
# For the train set (replace by valid or test as needed)
dataset_pg_list = [Data(graph) for graph in dataset_hf["train"]]
dataset_pg = DataLoader(dataset_pg_list)
```

## Dataset Structure

### Data Properties
| property | value |
|---|---|
| #graphs | 9,833 |
| average #nodes | 17.6 |
| average #edges | 35.8 |

### Data Fields

Each row of a given file is a graph, with: 
- `node_feat` (list: #nodes x #node-features): nodes
- `edge_index` (list: 2 x #edges): pairs of nodes constituting edges
- `edge_attr` (list: #edges x #edge-features): for the aforementioned edges, contains their features
- `y` (list:  #labels): contains the number of labels available to predict
- `num_nodes` (int): number of nodes of the graph

### Data Splits

This data is split. It comes from the PyGeometric version of the dataset.

## Additional Information

### Licensing Information
The dataset has been released under MIT license.

### Citation Information
```
@article{DBLP:journals/corr/abs-2003-00982,
  author    = {Vijay Prakash Dwivedi and
               Chaitanya K. Joshi and
               Thomas Laurent and
               Yoshua Bengio and
               Xavier Bresson},
  title     = {Benchmarking Graph Neural Networks},
  journal   = {CoRR},
  volume    = {abs/2003.00982},
  year      = {2020},
  url       = {https://arxiv.org/abs/2003.00982},
  eprinttype = {arXiv},
  eprint    = {2003.00982},
  timestamp = {Sat, 23 Jan 2021 01:14:30 +0100},
  biburl    = {https://dblp.org/rec/journals/corr/abs-2003-00982.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}

```