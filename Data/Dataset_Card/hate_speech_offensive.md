---
annotations_creators:
- expert-generated
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
- 10K<n<100K
source_datasets:
- original
task_categories:
- text-classification
task_ids: []
paperswithcode_id: hate-speech-and-offensive-language
pretty_name: Hate Speech and Offensive Language
tags:
- hate-speech-detection
dataset_info:
  features:
  - name: count
    dtype: int64
  - name: hate_speech_count
    dtype: int64
  - name: offensive_language_count
    dtype: int64
  - name: neither_count
    dtype: int64
  - name: class
    dtype:
      class_label:
        names:
          '0': hate speech
          '1': offensive language
          '2': neither
  - name: tweet
    dtype: string
  splits:
  - name: train
    num_bytes: 3207826
    num_examples: 24783
  download_size: 2546446
  dataset_size: 3207826
train-eval-index:
- config: default
  task: text-classification
  task_id: multi_class_classification
  splits:
    train_split: train
  col_mapping:
    tweet: text
    label: target
  metrics:
  - type: accuracy
    name: Accuracy
  - type: f1
    name: F1 macro
    args:
      average: macro
  - type: f1
    name: F1 micro
    args:
      average: micro
  - type: f1
    name: F1 weighted
    args:
      average: weighted
  - type: precision
    name: Precision macro
    args:
      average: macro
  - type: precision
    name: Precision micro
    args:
      average: micro
  - type: precision
    name: Precision weighted
    args:
      average: weighted
  - type: recall
    name: Recall macro
    args:
      average: macro
  - type: recall
    name: Recall micro
    args:
      average: micro
  - type: recall
    name: Recall weighted
    args:
      average: weighted
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

- **Homepage:** https://github.com/t-davidson/hate-speech-and-offensive-language
- **Repository:** https://github.com/t-davidson/hate-speech-and-offensive-language
- **Paper:** https://arxiv.org/abs/1703.04009
- **Leaderboard:**
- **Point of Contact:** https://docs.google.com/forms/d/e/1FAIpQLSdrPNlfVBlqxun2tivzAtsZaOoPC5YYMocn-xscCgeRakLXHg/viewform?usp=pp_url&entry.1506871634&entry.147453066&entry.1390333885&entry.516829772

### Dataset Summary

An annotated dataset for hate speech and offensive language detection on tweets.

### Supported Tasks and Leaderboards

[More Information Needed]

### Languages
English (`en`)

## Dataset Structure

### Data Instances
```
{
"count": 3,
 "hate_speech_annotation": 0,
 "offensive_language_annotation": 0,
 "neither_annotation": 3,
 "label": 2,  # "neither"
 "tweet": "!!! RT @mayasolovely: As a woman you shouldn't complain about cleaning up your house. &amp; as a man you should always take the trash out...")
}
```

### Data Fields
```
count: (Integer) number of users who coded each tweet (min is 3, sometimes more users coded a tweet when judgments were determined to be unreliable,
hate_speech_annotation: (Integer) number of users who judged the tweet to be hate speech,
offensive_language_annotation: (Integer) number of users who judged the tweet to be offensive,
neither_annotation: (Integer) number of users who judged the tweet to be neither offensive nor non-offensive,
label: (Class Label) class label for majority of CF users (0: 'hate-speech', 1: 'offensive-language' or 2: 'neither'),
tweet: (string)
```

### Data Splits
This dataset is not splitted, only the train split is available.

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
Usernames are not anonymized in the dataset.


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
MIT License

### Citation Information
@inproceedings{hateoffensive,
  title = {Automated Hate Speech Detection and the Problem of Offensive Language},
  author = {Davidson, Thomas and Warmsley, Dana and Macy, Michael and Weber, Ingmar}, 
  booktitle = {Proceedings of the 11th International AAAI Conference on Web and Social Media},
  series = {ICWSM '17},
  year = {2017},
  location = {Montreal, Canada},
  pages = {512-515}
  }

### Contributions

Thanks to [@hugoabonizio](https://github.com/hugoabonizio) for adding this dataset.