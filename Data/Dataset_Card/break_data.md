---
annotations_creators:
- crowdsourced
language_creators:
- crowdsourced
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
- text2text-generation
task_ids:
- open-domain-abstractive-qa
paperswithcode_id: break
pretty_name: BREAK
dataset_info:
- config_name: QDMR-high-level
  features:
  - name: question_id
    dtype: string
  - name: question_text
    dtype: string
  - name: decomposition
    dtype: string
  - name: operators
    dtype: string
  - name: split
    dtype: string
  splits:
  - name: test
    num_bytes: 482339
    num_examples: 3195
  - name: train
    num_bytes: 5148086
    num_examples: 17503
  - name: validation
    num_bytes: 914780
    num_examples: 3130
  download_size: 15971078
  dataset_size: 6545205
- config_name: QDMR-high-level-lexicon
  features:
  - name: source
    dtype: string
  - name: allowed_tokens
    dtype: string
  splits:
  - name: test
    num_bytes: 4240755
    num_examples: 3195
  - name: train
    num_bytes: 23234518
    num_examples: 17503
  - name: validation
    num_bytes: 4158679
    num_examples: 3130
  download_size: 15971078
  dataset_size: 31633952
- config_name: QDMR
  features:
  - name: question_id
    dtype: string
  - name: question_text
    dtype: string
  - name: decomposition
    dtype: string
  - name: operators
    dtype: string
  - name: split
    dtype: string
  splits:
  - name: test
    num_bytes: 900632
    num_examples: 8069
  - name: train
    num_bytes: 12790466
    num_examples: 44321
  - name: validation
    num_bytes: 2237472
    num_examples: 7760
  download_size: 15971078
  dataset_size: 15928570
- config_name: QDMR-lexicon
  features:
  - name: source
    dtype: string
  - name: allowed_tokens
    dtype: string
  splits:
  - name: test
    num_bytes: 10331822
    num_examples: 8069
  - name: train
    num_bytes: 56913064
    num_examples: 44321
  - name: validation
    num_bytes: 9936933
    num_examples: 7760
  download_size: 15971078
  dataset_size: 77181819
- config_name: logical-forms
  features:
  - name: question_id
    dtype: string
  - name: question_text
    dtype: string
  - name: decomposition
    dtype: string
  - name: operators
    dtype: string
  - name: split
    dtype: string
  - name: program
    dtype: string
  splits:
  - name: test
    num_bytes: 927038
    num_examples: 8006
  - name: train
    num_bytes: 19821676
    num_examples: 44098
  - name: validation
    num_bytes: 3504893
    num_examples: 7719
  download_size: 15971078
  dataset_size: 24253607
---

# Dataset Card for "break_data"

## Table of Contents
- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
  - [Supported Tasks and Leaderboards](#supported-tasks-and-leaderboards)
  - [Languages](#languages)
- [Dataset Structure](#dataset-structure)
  - [Data Instances](#data-instances)
  - [Data Fields](#data-fields)
  - [Data Splits](#data-splits)
- [Dataset Creation](#dataset-creation)
  - [Curation Rationale](#curation-rationale)
  - [Source Data](#source-data)
  - [Annotations](#annotations)
  - [Personal and Sensitive Information](#personal-and-sensitive-information)
- [Considerations for Using the Data](#considerations-for-using-the-data)
  - [Social Impact of Dataset](#social-impact-of-dataset)
  - [Discussion of Biases](#discussion-of-biases)
  - [Other Known Limitations](#other-known-limitations)
- [Additional Information](#additional-information)
  - [Dataset Curators](#dataset-curators)
  - [Licensing Information](#licensing-information)
  - [Citation Information](#citation-information)
  - [Contributions](#contributions)

## Dataset Description

- **Homepage:** [https://github.com/allenai/Break](https://github.com/allenai/Break)
- **Repository:** [More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)
- **Paper:** [More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)
- **Point of Contact:** [More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)
- **Size of downloaded dataset files:** 76.16 MB
- **Size of the generated dataset:** 148.34 MB
- **Total amount of disk used:** 224.49 MB

### Dataset Summary

Break is a human annotated dataset of natural language questions and their Question Decomposition Meaning Representations
(QDMRs). Break consists of 83,978 examples sampled from 10 question answering datasets over text, images and databases.
This repository contains the Break dataset along with information on the exact data format.

### Supported Tasks and Leaderboards

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Languages

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

## Dataset Structure

### Data Instances

#### QDMR

- **Size of downloaded dataset files:** 15.23 MB
- **Size of the generated dataset:** 15.19 MB
- **Total amount of disk used:** 30.42 MB

An example of 'validation' looks as follows.
```
{
    "decomposition": "return flights ;return #1 from  denver ;return #2 to philadelphia ;return #3 if  available",
    "operators": "['select', 'filter', 'filter', 'filter']",
    "question_id": "ATIS_dev_0",
    "question_text": "what flights are available tomorrow from denver to philadelphia ",
    "split": "dev"
}
```

#### QDMR-high-level

- **Size of downloaded dataset files:** 15.23 MB
- **Size of the generated dataset:** 6.24 MB
- **Total amount of disk used:** 21.47 MB

An example of 'train' looks as follows.
```
{
    "decomposition": "return ground transportation ;return #1 which  is  available ;return #2 from  the pittsburgh airport ;return #3 to downtown ;return the cost of #4",
    "operators": "['select', 'filter', 'filter', 'filter', 'project']",
    "question_id": "ATIS_dev_102",
    "question_text": "what ground transportation is available from the pittsburgh airport to downtown and how much does it cost ",
    "split": "dev"
}
```

#### QDMR-high-level-lexicon

- **Size of downloaded dataset files:** 15.23 MB
- **Size of the generated dataset:** 30.17 MB
- **Total amount of disk used:** 45.40 MB

An example of 'train' looks as follows.
```
This example was too long and was cropped:

{
    "allowed_tokens": "\"['higher than', 'same as', 'what ', 'and ', 'than ', 'at most', 'he', 'distinct', 'House', 'two', 'at least', 'or ', 'date', 'o...",
    "source": "What office, also held by a member of the Maine House of Representatives, did James K. Polk hold before he was president?"
}
```

#### QDMR-lexicon

- **Size of downloaded dataset files:** 15.23 MB
- **Size of the generated dataset:** 73.61 MB
- **Total amount of disk used:** 88.84 MB

An example of 'validation' looks as follows.
```
This example was too long and was cropped:

{
    "allowed_tokens": "\"['higher than', 'same as', 'what ', 'and ', 'than ', 'at most', 'distinct', 'two', 'at least', 'or ', 'date', 'on ', '@@14@@', ...",
    "source": "what flights are available tomorrow from denver to philadelphia "
}
```

#### logical-forms

- **Size of downloaded dataset files:** 15.23 MB
- **Size of the generated dataset:** 23.13 MB
- **Total amount of disk used:** 38.36 MB

An example of 'train' looks as follows.
```
{
    "decomposition": "return ground transportation ;return #1 which  is  available ;return #2 from  the pittsburgh airport ;return #3 to downtown ;return the cost of #4",
    "operators": "['select', 'filter', 'filter', 'filter', 'project']",
    "program": "some program",
    "question_id": "ATIS_dev_102",
    "question_text": "what ground transportation is available from the pittsburgh airport to downtown and how much does it cost ",
    "split": "dev"
}
```

### Data Fields

The data fields are the same among all splits.

#### QDMR
- `question_id`: a `string` feature.
- `question_text`: a `string` feature.
- `decomposition`: a `string` feature.
- `operators`: a `string` feature.
- `split`: a `string` feature.

#### QDMR-high-level
- `question_id`: a `string` feature.
- `question_text`: a `string` feature.
- `decomposition`: a `string` feature.
- `operators`: a `string` feature.
- `split`: a `string` feature.

#### QDMR-high-level-lexicon
- `source`: a `string` feature.
- `allowed_tokens`: a `string` feature.

#### QDMR-lexicon
- `source`: a `string` feature.
- `allowed_tokens`: a `string` feature.

#### logical-forms
- `question_id`: a `string` feature.
- `question_text`: a `string` feature.
- `decomposition`: a `string` feature.
- `operators`: a `string` feature.
- `split`: a `string` feature.
- `program`: a `string` feature.

### Data Splits

|         name          |train|validation|test|
|-----------------------|----:|---------:|---:|
|QDMR                   |44321|      7760|8069|
|QDMR-high-level        |17503|      3130|3195|
|QDMR-high-level-lexicon|17503|      3130|3195|
|QDMR-lexicon           |44321|      7760|8069|
|logical-forms          |44098|      7719|8006|

## Dataset Creation

### Curation Rationale

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Source Data

#### Initial Data Collection and Normalization

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

#### Who are the source language producers?

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Annotations

#### Annotation process

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

#### Who are the annotators?

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Personal and Sensitive Information

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

## Considerations for Using the Data

### Social Impact of Dataset

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Discussion of Biases

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Other Known Limitations

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

## Additional Information

### Dataset Curators

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Licensing Information

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Citation Information

```
@article{Wolfson2020Break,
  title={Break It Down: A Question Understanding Benchmark},
  author={Wolfson, Tomer and Geva, Mor and Gupta, Ankit and Gardner, Matt and Goldberg, Yoav and Deutch, Daniel and Berant, Jonathan},
  journal={Transactions of the Association for Computational Linguistics},
  year={2020},
}
```

### Contributions

Thanks to [@patrickvonplaten](https://github.com/patrickvonplaten), [@lewtun](https://github.com/lewtun), [@thomwolf](https://github.com/thomwolf) for adding this dataset.