---
annotations_creators:
- expert-generated
language_creators:
- expert-generated
language:
- fa
license:
- cc-by-nc-sa-4.0
multilinguality:
- monolingual
size_categories:
- 1K<n<10K
source_datasets:
- extended|translated|mnli
task_categories:
- textual-entailment
- natural-language-inference
task_ids:
- textual-entailment
- natural-language-inference
---

# Dataset Card for PersiNLU (Textual Entailment)

## Table of Contents
- [Dataset Card for PersiNLU (Textual Entailment)](#dataset-card-for-persi_nlu_entailment)
  - [Table of Contents](#table-of-contents)
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
      - [Initial Data Collection and Normalization](#initial-data-collection-and-normalization)
      - [Who are the source language producers?](#who-are-the-source-language-producers)
    - [Annotations](#annotations)
      - [Annotation process](#annotation-process)
      - [Who are the annotators?](#who-are-the-annotators)
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

- **Homepage:** [Github](https://github.com/persiannlp/parsinlu/)
- **Repository:** [Github](https://github.com/persiannlp/parsinlu/)
- **Paper:** [Arxiv](https://arxiv.org/abs/2012.06154)
- **Leaderboard:** 
- **Point of Contact:** d.khashabi@gmail.com

### Dataset Summary

A Persian textual entailment task (deciding `sent1` entails `sent2`). 
The questions are partially translated from the SNLI dataset and partially generated by expert annotators. 

### Supported Tasks and Leaderboards

[More Information Needed]

### Languages

The text dataset is in Persian (`fa`).

## Dataset Structure

### Data Instances

Here is an example from the dataset: 
```json 
{
  "sent1": "سالها است که کنگره در تلاش است تا اثربخشی مدیریت اطلاعات و فناوری را در دولت فدرال افزایش دهد.",
  "sent2": "کنگره بودجه ویژه ای برای مدیریت اطلاعات و فناوری در دولت فدرال دارد.",
  "label": "n",
  "category": "translation-train"
}
```

### Data Fields

- `sent1`: the first sentence.
- `sent2`: the second sentence. 
- `source`: whether the questions are translated from MNLI (`translation-.`) or they're written by native speakers (`natural-.`).   
- `label`: `e` if `sent2` is entailed from `sent1`; `c` if `sent2` is contradictory to `sent1`; `n` if the two sentences are neutral.     

### Data Splits

The train/dev/test splits contains 756/271/1751 samples.

## Dataset Creation

### Curation Rationale

For details, check [the corresponding draft](https://arxiv.org/abs/2012.06154).

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

CC BY-NC-SA 4.0 License 

### Citation Information
```bibtex 
@article{huggingface:dataset,
    title = {ParsiNLU: A Suite of Language Understanding Challenges for Persian},
    authors = {Khashabi, Daniel and Cohan, Arman and Shakeri, Siamak and Hosseini, Pedram and Pezeshkpour, Pouya and Alikhani, Malihe and Aminnaseri, Moin and Bitaab, Marzieh and Brahman, Faeze and Ghazarian, Sarik and others},
    year={2020}
    journal = {arXiv e-prints},
    eprint = {2012.06154},    
}
```

### Contributions

Thanks to [@danyaljj](https://github.com/danyaljj) for adding this dataset.
