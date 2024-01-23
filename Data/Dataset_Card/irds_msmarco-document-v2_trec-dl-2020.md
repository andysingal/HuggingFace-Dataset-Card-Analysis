---
pretty_name: '`msmarco-document-v2/trec-dl-2020`'
viewer: false
source_datasets: ['irds/msmarco-document-v2']
task_categories:
- text-retrieval
---

# Dataset Card for `msmarco-document-v2/trec-dl-2020`

The `msmarco-document-v2/trec-dl-2020` dataset, provided by the [ir-datasets](https://ir-datasets.com/) package.
For more information about the dataset, see the [documentation](https://ir-datasets.com/msmarco-document-v2#msmarco-document-v2/trec-dl-2020).

# Data

This dataset provides:
 - `queries` (i.e., topics); count=200
 - `qrels`: (relevance assessments); count=7,942

 - For `docs`, use [`irds/msmarco-document-v2`](https://huggingface.co/datasets/irds/msmarco-document-v2)

This dataset is used by: [`msmarco-document-v2_trec-dl-2020_judged`](https://huggingface.co/datasets/irds/msmarco-document-v2_trec-dl-2020_judged)


## Usage

```python
from datasets import load_dataset

queries = load_dataset('irds/msmarco-document-v2_trec-dl-2020', 'queries')
for record in queries:
    record # {'query_id': ..., 'text': ...}

qrels = load_dataset('irds/msmarco-document-v2_trec-dl-2020', 'qrels')
for record in qrels:
    record # {'query_id': ..., 'doc_id': ..., 'relevance': ..., 'iteration': ...}

```

Note that calling `load_dataset` will download the dataset (or provide access instructions when it's not public) and make a copy of the
data in 🤗 Dataset format.

## Citation Information

```
@inproceedings{Craswell2020TrecDl,
  title={Overview of the TREC 2020 deep learning track},
  author={Nick Craswell and Bhaskar Mitra and Emine Yilmaz and Daniel Campos},
  booktitle={TREC},
  year={2020}
}
@inproceedings{Bajaj2016Msmarco,
  title={MS MARCO: A Human Generated MAchine Reading COmprehension Dataset},
  author={Payal Bajaj, Daniel Campos, Nick Craswell, Li Deng, Jianfeng Gao, Xiaodong Liu, Rangan Majumder, Andrew McNamara, Bhaskar Mitra, Tri Nguyen, Mir Rosenberg, Xia Song, Alina Stoica, Saurabh Tiwary, Tong Wang},
  booktitle={InCoCo@NIPS},
  year={2016}
}
```