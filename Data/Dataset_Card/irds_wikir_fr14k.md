---
pretty_name: '`wikir/fr14k`'
viewer: false
source_datasets: []
task_categories:
- text-retrieval
---

# Dataset Card for `wikir/fr14k`

The `wikir/fr14k` dataset, provided by the [ir-datasets](https://ir-datasets.com/) package.
For more information about the dataset, see the [documentation](https://ir-datasets.com/wikir#wikir/fr14k).

# Data

This dataset provides:
 - `docs` (documents, i.e., the corpus); count=736,616


## Usage

```python
from datasets import load_dataset

docs = load_dataset('irds/wikir_fr14k', 'docs')
for record in docs:
    record # {'doc_id': ..., 'text': ...}

```

Note that calling `load_dataset` will download the dataset (or provide access instructions when it's not public) and make a copy of the
data in 🤗 Dataset format.

## Citation Information

```
@inproceedings{Frej2020Wikir,
  title={WIKIR: A Python toolkit for building a large-scale Wikipedia-based English Information Retrieval Dataset},
  author={Jibril Frej and Didier Schwab and Jean-Pierre Chevallet},
  booktitle={LREC},
  year={2020}
}
@inproceedings{Frej2020MlWikir,
  title={MLWIKIR: A Python Toolkit for Building Large-scale Wikipedia-based Information Retrieval Datasets in Chinese, English, French, Italian, Japanese, Spanish and More},
  author={Jibril Frej and Didier Schwab and Jean-Pierre Chevallet},
  booktitle={CIRCLE},
  year={2020}
}
```
