---
annotations_creators:
- expert-generated
language_creators:
- other
language:
- pl
license:
- bsd-3-clause
multilinguality:
- monolingual
size_categories:
- 1K<n<10K
source_datasets:
- original
task_categories:
- text-classification
task_ids:
- sentiment-classification
pretty_name: polemo2
dataset_info:
- config_name: in
  features:
  - name: sentence
    dtype: string
  - name: target
    dtype:
      class_label:
        names:
          '0': __label__meta_amb
          '1': __label__meta_minus_m
          '2': __label__meta_plus_m
          '3': __label__meta_zero
  splits:
  - name: train
    num_bytes: 4810215
    num_examples: 5783
  - name: test
    num_bytes: 582052
    num_examples: 722
  - name: validation
    num_bytes: 593530
    num_examples: 723
  download_size: 2350339
  dataset_size: 5985797
- config_name: out
  features:
  - name: sentence
    dtype: string
  - name: target
    dtype:
      class_label:
        names:
          '0': __label__meta_amb
          '1': __label__meta_minus_m
          '2': __label__meta_plus_m
          '3': __label__meta_zero
  splits:
  - name: train
    num_bytes: 4810215
    num_examples: 5783
  - name: test
    num_bytes: 309790
    num_examples: 494
  - name: validation
    num_bytes: 310977
    num_examples: 494
  download_size: 2139891
  dataset_size: 5430982
---

# Dataset Card for [Dataset Name]

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

- **Homepage:**
  https://clarin-pl.eu/dspace/handle/11321/710
- **Repository:**
- **Paper:**
- **Leaderboard:**
- **Point of Contact:**

### Dataset Summary

The PolEmo2.0 is a set of online reviews from medicine and hotels domains. The task is to predict the sentiment of a review. There are two separate test sets, to allow for in-domain (medicine and hotels) as well as out-of-domain (products and university) validation.

### Supported Tasks and Leaderboards

[More Information Needed]

### Languages

Polish

## Dataset Structure

### Data Instances

[More Information Needed]

### Data Fields

- sentence: string, the review
- target: sentiment of the sentence class

The same tag system is used in plWordNet Emo for lexical units: [+m] (strong positive), [+s] (weak positive), [-m] (strong negative), [-s] (weak negative), [amb] (ambiguous) and [0] (neutral).

Note that the test set doesn't have targets so -1 is used instead

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

Dataset provided for research purposes only. Please check dataset license for additional information.

## Additional Information

### Dataset Curators

[More Information Needed]

### Licensing Information

CC BY-NC-SA 4.0

### Citation Information

[More Information Needed]

### Contributions

Thanks to [@abecadel](https://github.com/abecadel) for adding this dataset.