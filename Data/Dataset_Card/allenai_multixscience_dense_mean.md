---
annotations_creators:
- found
language_creators:
- found
language:
- en
license:
- unknown
multilinguality:
- monolingual
size_categories:
- 10K<n<100K
source_datasets:
- original
task_categories:
- summarization
paperswithcode_id: multi-xscience
pretty_name: Multi-XScience
---

This is a copy of the [Multi-XScience](https://huggingface.co/datasets/multi_x_science_sum) dataset, except the input source documents of its `train`, `validation` and `test` splits have been replaced by a __dense__ retriever. The retrieval pipeline used:

- __query__: The `related_work` field of each example
- __corpus__: The union of all documents in the `train`, `validation` and `test` splits
- __retriever__: [`facebook/contriever-msmarco`](https://huggingface.co/facebook/contriever-msmarco) via [PyTerrier](https://pyterrier.readthedocs.io/en/latest/) with default settings
- __top-k strategy__: `"max"`, i.e. the number of documents retrieved, `k`, is set as the maximum number of documents seen across examples in this dataset, in this case `k==4`

Retrieval results on the `train` set:

| Recall@100 | Rprec | Precision@k | Recall@k |
| ----------- | ----------- | ----------- | ----------- |
| 0.5270 | 0.2005 | 0.1551 | 0.2357 |

Retrieval results on the `validation` set:

| Recall@100 | Rprec | Precision@k | Recall@k |
| ----------- | ----------- | ----------- | ----------- |
| 0.5310 | 0.2026 | 0.1603 | 0.2432 |

Retrieval results on the `test` set:

| Recall@100 | Rprec | Precision@k | Recall@k |
| ----------- | ----------- | ----------- | ----------- |
| 0.5229 | 0.2081 | 0.1612 | 0.2440 |