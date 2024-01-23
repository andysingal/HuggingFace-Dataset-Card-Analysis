---
annotations_creators:
- crowdsourced
language_creators:
- found
language:
- en
license:
- unknown
multilinguality:
- monolingual
size_categories:
- 100K<n<1M
source_datasets:
- original
task_categories:
- multiple-choice
- text-classification
task_ids:
- natural-language-inference
paperswithcode_id: art-dataset
pretty_name: Abductive Reasoning in narrative Text
tags:
- abductive-natural-language-inference
dataset_info:
  features:
  - name: observation_1
    dtype: string
  - name: observation_2
    dtype: string
  - name: hypothesis_1
    dtype: string
  - name: hypothesis_2
    dtype: string
  - name: label
    dtype:
      class_label:
        names:
          '0': '0'
          '1': '1'
          '2': '2'
  config_name: anli
  splits:
  - name: validation
    num_bytes: 312314
    num_examples: 1532
  - name: train
    num_bytes: 34046304
    num_examples: 169654
  download_size: 5118294
  dataset_size: 34358618
---

# Dataset Card for "art"

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

- **Homepage:** [https://leaderboard.allenai.org/anli/submissions/get-started](https://leaderboard.allenai.org/anli/submissions/get-started)
- **Repository:** https://github.com/allenai/abductive-commonsense-reasoning
- **Paper:** [Abductive Commonsense Reasoning](https://arxiv.org/abs/1908.05739)
- **Point of Contact:** [More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)
- **Size of downloaded dataset files:** 4.88 MB
- **Size of the generated dataset:** 32.77 MB
- **Total amount of disk used:** 37.65 MB

### Dataset Summary

ART consists of over 20k commonsense narrative contexts and 200k explanations.

The Abductive Natural Language Inference Dataset from AI2.

### Supported Tasks and Leaderboards

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Languages

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

## Dataset Structure

### Data Instances

#### anli

- **Size of downloaded dataset files:** 4.88 MB
- **Size of the generated dataset:** 32.77 MB
- **Total amount of disk used:** 37.65 MB

An example of 'train' looks as follows.
```
{
    "hypothesis_1": "Chad's car had all sorts of other problems besides alignment.",
    "hypothesis_2": "Chad's car had all sorts of benefits other than being sexy.",
    "label": 1,
    "observation_1": "Chad went to get the wheel alignment measured on his car.",
    "observation_2": "The mechanic provided a working alignment with new body work."
}
```

### Data Fields

The data fields are the same among all splits.

#### anli
- `observation_1`: a `string` feature.
- `observation_2`: a `string` feature.
- `hypothesis_1`: a `string` feature.
- `hypothesis_2`: a `string` feature.
- `label`: a classification label, with possible values including `0` (0), `1` (1), `2` (2).

### Data Splits

|name|train |validation|
|----|-----:|---------:|
|anli|169654|      1532|

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
@inproceedings{Bhagavatula2020Abductive,
  title={Abductive Commonsense Reasoning},
  author={Chandra Bhagavatula and Ronan Le Bras and Chaitanya Malaviya and Keisuke Sakaguchi and Ari Holtzman and Hannah Rashkin and Doug Downey and Wen-tau Yih and Yejin Choi},
  booktitle={International Conference on Learning Representations},
  year={2020},
  url={https://openreview.net/forum?id=Byg1v1HKDB}
}
```

### Contributions

Thanks to [@patrickvonplaten](https://github.com/patrickvonplaten), [@thomwolf](https://github.com/thomwolf), [@mariamabarham](https://github.com/mariamabarham), [@lewtun](https://github.com/lewtun), [@lhoestq](https://github.com/lhoestq) for adding this dataset.