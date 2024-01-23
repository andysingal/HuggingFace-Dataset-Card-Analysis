---
annotations_creators:
- found
language_creators:
- found
language:
- en
- ku
- tr
license:
- unknown
multilinguality:
- translation
size_categories:
- 10K<n<100K
- 1K<n<10K
source_datasets:
- original
task_categories:
- translation
task_ids: []
paperswithcode_id: bianet
pretty_name: Bianet
configs:
- en-to-ku
- en-to-tr
- en_to_ku
- en_to_tr
- ku-to-tr
- ku_to_tr
dataset_info:
- config_name: en_to_ku
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - en
        - ku
  splits:
  - name: train
    num_bytes: 1800806
    num_examples: 6402
  download_size: 622420
  dataset_size: 1800806
- config_name: en_to_tr
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - en
        - tr
  splits:
  - name: train
    num_bytes: 10231043
    num_examples: 34770
  download_size: 3544116
  dataset_size: 10231043
- config_name: ku_to_tr
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - ku
        - tr
  splits:
  - name: train
    num_bytes: 2086550
    num_examples: 7325
  download_size: 725227
  dataset_size: 2086550
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

- **Homepage:** [Bianet](http://opus.nlpl.eu/Bianet.php)
- **Repository:**
- **Paper:** [Ataman, D. (2018) Bianet: A Parallel News Corpus in Turkish, Kurdish and English. In Proceedings of the LREC 2018 Workshop MLP-Moment. pp. 14-17. pdf](http://lrec-conf.org/workshops/lrec2018/W19/pdf/6_W19.pdf)
- **Leaderboard:**
- **Point of Contact:**

### Dataset Summary

A parallel news corpus in Turkish, Kurdish and English;
Bianet collects 3,214 Turkish articles with their sentence-aligned Kurdish or English translations from the Bianet online newspaper.

3 languages, 3 bitexts
total number of files: 6
total number of tokens: 2.25M
total number of sentence fragments: 0.14M

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

CC-BY-SA-4.0

### Citation Information

@InProceedings{ATAMAN18.6,
  author = {Duygu Ataman},
  title = {Bianet: A Parallel News Corpus in Turkish, Kurdish and English},
  booktitle = {Proceedings of the Eleventh International Conference on Language Resources and Evaluation (LREC 2018)},
  year = {2018},
  month = {may},
  date = {7-12},
  location = {Miyazaki, Japan},
  editor = {Jinhua Du and Mihael Arcan and Qun Liu and Hitoshi Isahara},
  publisher = {European Language Resources Association (ELRA)},
  address = {Paris, France},
  isbn = {979-10-95546-15-3},
  language = {english}
  }

### Contributions

Thanks to [@param087](https://github.com/param087) for adding this dataset.