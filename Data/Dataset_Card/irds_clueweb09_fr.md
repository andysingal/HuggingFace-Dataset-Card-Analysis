---
pretty_name: '`clueweb09/fr`'
viewer: false
source_datasets: []
task_categories:
- text-retrieval
---

# Dataset Card for `clueweb09/fr`

The `clueweb09/fr` dataset, provided by the [ir-datasets](https://ir-datasets.com/) package.
For more information about the dataset, see the [documentation](https://ir-datasets.com/clueweb09#clueweb09/fr).

# Data

This dataset provides:
 - `docs` (documents, i.e., the corpus); count=50,883,172


## Usage

```python
from datasets import load_dataset

docs = load_dataset('irds/clueweb09_fr', 'docs')
for record in docs:
    record # {'doc_id': ..., 'url': ..., 'date': ..., 'http_headers': ..., 'body': ..., 'body_content_type': ...}

```

Note that calling `load_dataset` will download the dataset (or provide access instructions when it's not public) and make a copy of the
data in 🤗 Dataset format.