---
annotations_creators:
- crowdsourced
language_creators:
- found
language:
- zh
license:
- unknown
multilinguality:
- monolingual
size_categories:
- 10K<n<100K
source_datasets:
- original
task_categories:
- token-classification
task_ids:
- named-entity-recognition
pretty_name: MSRA NER
dataset_info:
  features:
  - name: id
    dtype: string
  - name: tokens
    sequence: string
  - name: ner_tags
    sequence:
      class_label:
        names:
          '0': O
          '1': B-PER
          '2': I-PER
          '3': B-ORG
          '4': I-ORG
          '5': B-LOC
          '6': I-LOC
  config_name: msra_ner
  splits:
  - name: train
    num_bytes: 33323074
    num_examples: 45001
  - name: test
    num_bytes: 2642934
    num_examples: 3443
  download_size: 15156606
  dataset_size: 35966008
train-eval-index:
- config: msra_ner
  task: token-classification
  task_id: entity_extraction
  splits:
    train_split: train
    eval_split: test
  col_mapping:
    tokens: tokens
    ner_tags: tags
  metrics:
  - type: seqeval
    name: seqeval
---

# Dataset Card for MSRA NER

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

- **Homepage:** [Github](https://github.com/OYE93/Chinese-NLP-Corpus/tree/master/NER/MSRA)
- **Repository:** [Github](https://github.com/OYE93/Chinese-NLP-Corpus)
- **Paper:**
- **Leaderboard:**
- **Point of Contact:**

### Dataset Summary

[More Information Needed]

### Supported Tasks and Leaderboards

[More Information Needed]

### Languages

[More Information Needed]

## Dataset Structure

### Data Instances

[More Information Needed]

### Data Fields

[More Information Needed]

### Data Splits

[More Information Needed]

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

[More Information Needed]

### Citation Information

[More Information Needed]

### Contributions

Thanks to [@JetRunner](https://github.com/JetRunner) for adding this dataset.