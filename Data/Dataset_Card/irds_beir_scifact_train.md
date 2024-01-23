---
pretty_name: '`beir/scifact/train`'
viewer: false
source_datasets: ['irds/beir_scifact']
task_categories:
- text-retrieval
---

# Dataset Card for `beir/scifact/train`

The `beir/scifact/train` dataset, provided by the [ir-datasets](https://ir-datasets.com/) package.
For more information about the dataset, see the [documentation](https://ir-datasets.com/beir#beir/scifact/train).

# Data

This dataset provides:
 - `queries` (i.e., topics); count=809
 - `qrels`: (relevance assessments); count=919

 - For `docs`, use [`irds/beir_scifact`](https://huggingface.co/datasets/irds/beir_scifact)

## Usage

```python
from datasets import load_dataset

queries = load_dataset('irds/beir_scifact_train', 'queries')
for record in queries:
    record # {'query_id': ..., 'text': ...}

qrels = load_dataset('irds/beir_scifact_train', 'qrels')
for record in qrels:
    record # {'query_id': ..., 'doc_id': ..., 'relevance': ..., 'iteration': ...}

```

Note that calling `load_dataset` will download the dataset (or provide access instructions when it's not public) and make a copy of the
data in 🤗 Dataset format.

## Citation Information

```
@inproceedings{Wadden2020Scifact,
    title = "Fact or Fiction: Verifying Scientific Claims",
    author = "Wadden, David  and
      Lin, Shanchuan  and
      Lo, Kyle  and
      Wang, Lucy Lu  and
      van Zuylen, Madeleine  and
      Cohan, Arman  and
      Hajishirzi, Hannaneh",
    booktitle = "Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP)",
    month = nov,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.emnlp-main.609",
    doi = "10.18653/v1/2020.emnlp-main.609",
    pages = "7534--7550"
}
@article{Thakur2021Beir,
  title = "BEIR: A Heterogenous Benchmark for Zero-shot Evaluation of Information Retrieval Models",
  author = "Thakur, Nandan and Reimers, Nils and Rücklé, Andreas and Srivastava, Abhishek and Gurevych, Iryna", 
  journal= "arXiv preprint arXiv:2104.08663",
  month = "4",
  year = "2021",
  url = "https://arxiv.org/abs/2104.08663",
}
```