---
annotations_creators:
- crowdsourced
language_creators:
- crowdsourced
language:
- en
license:
- cc-by-4.0
multilinguality:
- monolingual
size_categories:
- 1K<n<10K
source_datasets:
- extended|other-xsum
task_categories:
- summarization
task_ids: []
pretty_name: XSum Hallucination Annotations
tags:
- hallucinations
dataset_info:
- config_name: xsum_factuality
  features:
  - name: bbcid
    dtype: int32
  - name: system
    dtype: string
  - name: summary
    dtype: string
  - name: is_factual
    dtype:
      class_label:
        names:
          '0': 'no'
          '1': 'yes'
  - name: worker_id
    dtype: string
  splits:
  - name: train
    num_bytes: 800027
    num_examples: 5597
  download_size: 2864759
  dataset_size: 800027
- config_name: xsum_faithfulness
  features:
  - name: bbcid
    dtype: int32
  - name: system
    dtype: string
  - name: summary
    dtype: string
  - name: hallucination_type
    dtype:
      class_label:
        names:
          '0': intrinsic
          '1': extrinsic
  - name: hallucinated_span_start
    dtype: int32
  - name: hallucinated_span_end
    dtype: int32
  - name: worker_id
    dtype: string
  splits:
  - name: train
    num_bytes: 1750325
    num_examples: 11185
  download_size: 2864759
  dataset_size: 1750325
---

# Dataset Card for XSum Hallucination Annotations

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

- **Homepage:** [XSUM Hallucination Annotations Homepage](https://research.google/tools/datasets/xsum-hallucination-annotations/)
- **Repository:** [XSUM Hallucination Annotations Homepage](https://github.com/google-research-datasets/xsum_hallucination_annotations)
- **Paper:** [ACL Web](https://www.aclweb.org/anthology/2020.acl-main.173.pdf)
- **Point of Contact:** [xsum-hallucinations-acl20@google.com](mailto:xsum-hallucinations-acl20@google.com)

### Dataset Summary

Neural abstractive summarization models are highly prone to hallucinate content that is unfaithful to the input document. The popular metric such as ROUGE fails to show the severity of the problem. This dataset contains a large scale human evaluation of several neural abstractive summarization systems to better understand the types of hallucinations they produce. The dataset consists of faithfulness and factuality annotations of abstractive summaries for the XSum dataset. The dataset has crowdsourced 3 judgements for each of 500 x 5 document-system pairs. This will be a valuable resource to the abstractive summarization community.

### Supported Tasks and Leaderboards

* `summarization`: : The dataset can be used to train a model for Summarization,, which consists in summarizing a given document. Success on this task is typically measured by achieving a *high/low* [ROUGE Score](https://huggingface.co/metrics/rouge).

### Languages

The text in the dataset is in English which are abstractive summaries for the [XSum dataset](https://www.aclweb.org/anthology/D18-1206.pdf). The associated BCP-47 code is `en`.

## Dataset Structure

### Data Instances

##### Faithfulness annotations dataset

A typical data point consists of an ID referring to the news article(complete document), summary, and the hallucination span information.

An example from the XSum Faithfulness dataset looks as follows:

```
{
'bbcid': 34687720,
 'hallucinated_span_end': 114,
 'hallucinated_span_start': 1,
 'hallucination_type': 1,
 'summary': 'rory mcilroy will take a one-shot lead into the final round of the wgc-hsbc champions after carding a three-under',
 'system': 'BERTS2S',
 'worker_id': 'wid_0'
 }
```

##### Factuality annotations dataset

A typical data point consists of an ID referring to the news article(complete document), summary, and whether the summary is factual or not.

An example from the XSum Factuality dataset looks as follows:

```
{
'bbcid': 29911712,
 'is_factual': 0,
 'summary': 'more than 50 pupils at a bristol academy have been sent home from school because of a lack of uniform.',
 'system': 'BERTS2S',
 'worker_id': 'wid_0'
 }
```

### Data Fields

##### Faithfulness annotations dataset

Raters are shown the news article and the system summary, and are tasked with identifying and annotating the spans that aren't supported by the input article. The file contains the following columns:


- `bbcid`: Document id in the XSum corpus.
- `system`: Name of neural summarizer.
- `summary`: Summary generated by ‘system’.
- `hallucination_type`: Type of hallucination: intrinsic (0) or extrinsic (1)
- `hallucinated_span`: Hallucinated span in the ‘summary’.
- `hallucinated_span_start`: Index of the start of the hallucinated span.
- `hallucinated_span_end`: Index of the end of the hallucinated span.
- `worker_id`: Worker ID (one of 'wid_0', 'wid_1', 'wid_2')


The `hallucination_type` column has NULL value for some entries which have been replaced iwth `-1`.

##### Factuality annotations dataset

Raters are shown the news article and the hallucinated system summary, and are tasked with assessing the summary whether it is factual or not. The file contains the following columns:


- `bbcid1: Document id in the XSum corpus.
- `system`: Name of neural summarizer.
- `summary`: Summary generated by ‘system’.
- `is_factual`: Yes (1) or No (0)
- `worker_id`: Worker ID (one of 'wid_0', 'wid_1', 'wid_2')


The `is_factual` column has NULL value for some entries which have been replaced iwth `-1`.

### Data Splits

There is only a single split for both the Faithfulness annotations dataset and Factuality annotations dataset.

|                          | train |
|--------------------------|------:|
| Faithfulness annotations | 11185 |
| Factuality annotations   |  5597 |

## Dataset Creation

### Curation Rationale

[More Information Needed]

### Source Data

#### Initial Data Collection and Normalization

[More Information Needed]

#### Who are the source language producers?

[More Information Needed]

### Annotations

#### Annotation process

[More Information Needed]

#### Who are the annotators?

[More Information Needed]

### Personal and Sensitive Information

[More Information Needed]

## Considerations for Using the Data

### Social Impact of Dataset

[More Information Needed]

### Discussion of Biases

[More Information Needed]

### Other Known Limitations

[More Information Needed]

## Additional Information

### Dataset Curators

[More Information Needed]

### Licensing Information

[Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/legalcode)

### Citation Information

```
@InProceedings{maynez_acl20,
  author =      "Joshua Maynez and Shashi Narayan and Bernd Bohnet and Ryan Thomas Mcdonald",
  title =       "On Faithfulness and Factuality in Abstractive Summarization",
  booktitle =   "Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics",
  year =        "2020",
  pages = "1906--1919",
  address = "Online",
}
```


### Contributions

Thanks to [@vineeths96](https://github.com/vineeths96) for adding this dataset.