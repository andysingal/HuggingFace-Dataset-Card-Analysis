---
pretty_name: '`neumarco/zh`'
viewer: false
source_datasets: []
task_categories:
- text-retrieval
---

# Dataset Card for `neumarco/zh`

The `neumarco/zh` dataset, provided by the [ir-datasets](https://ir-datasets.com/) package.
For more information about the dataset, see the [documentation](https://ir-datasets.com/neumarco#neumarco/zh).

# Data

This dataset provides:
 - `docs` (documents, i.e., the corpus); count=8,841,823


This dataset is used by: [`neumarco_zh_dev`](https://huggingface.co/datasets/irds/neumarco_zh_dev), [`neumarco_zh_dev_judged`](https://huggingface.co/datasets/irds/neumarco_zh_dev_judged), [`neumarco_zh_dev_small`](https://huggingface.co/datasets/irds/neumarco_zh_dev_small), [`neumarco_zh_train`](https://huggingface.co/datasets/irds/neumarco_zh_train), [`neumarco_zh_train_judged`](https://huggingface.co/datasets/irds/neumarco_zh_train_judged)


## Usage

```python
from datasets import load_dataset

docs = load_dataset('irds/neumarco_zh', 'docs')
for record in docs:
    record # {'doc_id': ..., 'text': ...}

```

Note that calling `load_dataset` will download the dataset (or provide access instructions when it's not public) and make a copy of the
data in 🤗 Dataset format.