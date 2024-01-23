---
pretty_name: '`wikiclir/de`'
viewer: false
source_datasets: []
task_categories:
- text-retrieval
---

# Dataset Card for `wikiclir/de`

The `wikiclir/de` dataset, provided by the [ir-datasets](https://ir-datasets.com/) package.
For more information about the dataset, see the [documentation](https://ir-datasets.com/wikiclir#wikiclir/de).

# Data

This dataset provides:
 - `docs` (documents, i.e., the corpus); count=2,091,278
 - `queries` (i.e., topics); count=938,217
 - `qrels`: (relevance assessments); count=5,550,454


## Usage

```python
from datasets import load_dataset

docs = load_dataset('irds/wikiclir_de', 'docs')
for record in docs:
    record # {'doc_id': ..., 'title': ..., 'text': ...}

queries = load_dataset('irds/wikiclir_de', 'queries')
for record in queries:
    record # {'query_id': ..., 'text': ...}

qrels = load_dataset('irds/wikiclir_de', 'qrels')
for record in qrels:
    record # {'query_id': ..., 'doc_id': ..., 'relevance': ..., 'iteration': ...}

```

Note that calling `load_dataset` will download the dataset (or provide access instructions when it's not public) and make a copy of the
data in 🤗 Dataset format.

## Citation Information

```
@inproceedings{sasaki-etal-2018-cross,
    title = "Cross-Lingual Learning-to-Rank with Shared Representations",
    author = "Sasaki, Shota  and
      Sun, Shuo  and
      Schamoni, Shigehiko  and
      Duh, Kevin  and
      Inui, Kentaro",
    booktitle = "Proceedings of the 2018 Conference of the North {A}merican Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 2 (Short Papers)",
    month = jun,
    year = "2018",
    address = "New Orleans, Louisiana",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/N18-2073",
    doi = "10.18653/v1/N18-2073",
    pages = "458--463"
}
```