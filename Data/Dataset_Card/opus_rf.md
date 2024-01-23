---
annotations_creators:
- found
language_creators:
- expert-generated
language:
- de
- en
- es
- fr
- sv
license:
- unknown
multilinguality:
- multilingual
size_categories:
- n<1K
source_datasets:
- original
task_categories:
- translation
task_ids: []
paperswithcode_id: null
pretty_name: OpusRf
configs:
- de-en
- de-es
- de-fr
- de-sv
- en-es
- en-fr
- en-sv
- es-fr
- es-sv
- fr-sv
dataset_info:
- config_name: de-en
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - de
        - en
  splits:
  - name: train
    num_bytes: 38683
    num_examples: 177
  download_size: 16029
  dataset_size: 38683
- config_name: de-es
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - de
        - es
  splits:
  - name: train
    num_bytes: 2316
    num_examples: 24
  download_size: 2403
  dataset_size: 2316
- config_name: de-fr
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - de
        - fr
  splits:
  - name: train
    num_bytes: 41300
    num_examples: 173
  download_size: 16720
  dataset_size: 41300
- config_name: de-sv
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - de
        - sv
  splits:
  - name: train
    num_bytes: 37414
    num_examples: 178
  download_size: 15749
  dataset_size: 37414
- config_name: en-es
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - en
        - es
  splits:
  - name: train
    num_bytes: 2600
    num_examples: 25
  download_size: 2485
  dataset_size: 2600
- config_name: en-fr
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - en
        - fr
  splits:
  - name: train
    num_bytes: 39503
    num_examples: 175
  download_size: 16038
  dataset_size: 39503
- config_name: en-sv
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - en
        - sv
  splits:
  - name: train
    num_bytes: 35778
    num_examples: 180
  download_size: 15147
  dataset_size: 35778
- config_name: es-fr
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - es
        - fr
  splits:
  - name: train
    num_bytes: 2519
    num_examples: 21
  download_size: 2469
  dataset_size: 2519
- config_name: es-sv
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - es
        - sv
  splits:
  - name: train
    num_bytes: 3110
    num_examples: 28
  download_size: 2726
  dataset_size: 3110
- config_name: fr-sv
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - fr
        - sv
  splits:
  - name: train
    num_bytes: 38627
    num_examples: 175
  download_size: 15937
  dataset_size: 38627
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

- **Homepage:** http://opus.nlpl.eu/RF.php
- **Repository:**
- **Paper:** http://www.lrec-conf.org/proceedings/lrec2012/pdf/463_Paper.pdf
- **Leaderboard:** [More Information Needed]
- **Point of Contact:** [More Information Needed]

### Dataset Summary

RF is a tiny parallel corpus of the Declarations of the Swedish Government and its translations.

### Supported Tasks and Leaderboards

[More Information Needed]

### Languages

English (en), Spanish (es), German (de), French (fr), Swedish (sv)

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

```
@InProceedings{TIEDEMANN12.463,
  author = {J{\"o}rg Tiedemann},
  title = {Parallel Data, Tools and Interfaces in OPUS},
  booktitle = {Proceedings of the Eight International Conference on Language Resources and Evaluation (LREC'12)},
  year = {2012},
  month = {may},
  date = {23-25},
  address = {Istanbul, Turkey},
  editor = {Nicoletta Calzolari (Conference Chair) and Khalid Choukri and Thierry Declerck and Mehmet Ugur Dogan and Bente Maegaard and Joseph Mariani and Jan Odijk and Stelios Piperidis},
  publisher = {European Language Resources Association (ELRA)},
  isbn = {978-2-9517408-7-7},
  language = {english}
 }
```

### Contributions

Thanks to [@akshayb7](https://github.com/akshayb7) for adding this dataset.