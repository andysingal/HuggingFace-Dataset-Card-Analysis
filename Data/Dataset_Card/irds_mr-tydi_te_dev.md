---
pretty_name: '`mr-tydi/te/dev`'
viewer: false
source_datasets: ['irds/mr-tydi_te']
task_categories:
- text-retrieval
---

# Dataset Card for `mr-tydi/te/dev`

The `mr-tydi/te/dev` dataset, provided by the [ir-datasets](https://ir-datasets.com/) package.
For more information about the dataset, see the [documentation](https://ir-datasets.com/mr-tydi#mr-tydi/te/dev).

# Data

This dataset provides:
 - `queries` (i.e., topics); count=983
 - `qrels`: (relevance assessments); count=983

 - For `docs`, use [`irds/mr-tydi_te`](https://huggingface.co/datasets/irds/mr-tydi_te)

## Usage

```python
from datasets import load_dataset

queries = load_dataset('irds/mr-tydi_te_dev', 'queries')
for record in queries:
    record # {'query_id': ..., 'text': ...}

qrels = load_dataset('irds/mr-tydi_te_dev', 'qrels')
for record in qrels:
    record # {'query_id': ..., 'doc_id': ..., 'relevance': ..., 'iteration': ...}

```

Note that calling `load_dataset` will download the dataset (or provide access instructions when it's not public) and make a copy of the
data in 🤗 Dataset format.

## Citation Information

```
@article{Zhang2021MrTyDi,
  title={{Mr. TyDi}: A Multi-lingual Benchmark for Dense Retrieval}, 
  author={Xinyu Zhang and Xueguang Ma and Peng Shi and Jimmy Lin},
  year={2021},
  journal={arXiv:2108.08787},
}
@article{Clark2020TyDiQa,
    title={{TyDi QA}: A Benchmark for Information-Seeking Question Answering in Typologically Diverse Languages},
    author={Jonathan H. Clark and Eunsol Choi and Michael Collins and Dan Garrette and Tom Kwiatkowski and Vitaly Nikolaev and Jennimaria Palomaki},
    year={2020},
    journal={Transactions of the Association for Computational Linguistics}
}
```
