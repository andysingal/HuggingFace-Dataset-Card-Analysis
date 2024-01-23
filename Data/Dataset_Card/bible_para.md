---
annotations_creators:
- found
language_creators:
- found
language:
- acu
- af
- agr
- ake
- am
- amu
- ar
- bg
- bsn
- cak
- ceb
- ch
- chq
- chr
- cjp
- cni
- cop
- crp
- cs
- da
- de
- dik
- dje
- djk
- dop
- ee
- el
- en
- eo
- es
- et
- eu
- fi
- fr
- gbi
- gd
- gu
- gv
- he
- hi
- hr
- hu
- hy
- id
- is
- it
- ja
- jak
- jiv
- kab
- kbh
- kek
- kn
- ko
- la
- lt
- lv
- mam
- mi
- ml
- mr
- my
- ne
- nhg
- nl
- 'no'
- ojb
- pck
- pes
- pl
- plt
- pot
- ppk
- pt
- quc
- quw
- ro
- rom
- ru
- shi
- sk
- sl
- sn
- so
- sq
- sr
- ss
- sv
- syr
- te
- th
- tl
- tmh
- tr
- uk
- usp
- vi
- wal
- wo
- xh
- zh
- zu
license:
- cc0-1.0
multilinguality:
- multilingual
size_categories:
- 10K<n<100K
source_datasets:
- original
task_categories:
- translation
task_ids: []
paperswithcode_id: null
pretty_name: BiblePara
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
    num_bytes: 17262178
    num_examples: 62195
  download_size: 5440713
  dataset_size: 17262178
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
    num_bytes: 17536445
    num_examples: 62195
  download_size: 5470044
  dataset_size: 17536445
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
    num_bytes: 17105724
    num_examples: 62191
  download_size: 5418998
  dataset_size: 17105724
- config_name: en-fi
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - en
        - fi
  splits:
  - name: train
    num_bytes: 17486055
    num_examples: 62026
  download_size: 5506407
  dataset_size: 17486055
- config_name: en-no
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - en
        - 'no'
  splits:
  - name: train
    num_bytes: 16681323
    num_examples: 62107
  download_size: 5293164
  dataset_size: 16681323
- config_name: en-hi
  features:
  - name: id
    dtype: string
  - name: translation
    dtype:
      translation:
        languages:
        - en
        - hi
  splits:
  - name: train
    num_bytes: 27849361
    num_examples: 62073
  download_size: 6224765
  dataset_size: 27849361
---

# Dataset Card for BiblePara

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

- **Homepage:** http://opus.nlpl.eu/bible-uedin.php
- **Repository:** None
- **Paper:** https://link.springer.com/article/10.1007/s10579-014-9287-y
- **Leaderboard:** [More Information Needed]
- **Point of Contact:** [More Information Needed]

### Dataset Summary

To load a language pair which isn't part of the config, all you need to do is specify the language code as pairs.
You can find the valid pairs in Homepage section of Dataset Description: http://opus.nlpl.eu/bible-uedin.php
E.g.

`dataset = load_dataset("bible_para", lang1="fi", lang2="hi")`


### Supported Tasks and Leaderboards

[More Information Needed]

### Languages

[More Information Needed]

## Dataset Structure

### Data Instances

Here are some examples of questions and facts:


### Data Fields

[More Information Needed]

### Data Splits

[More Information Needed]

## Dataset Creation

### Curation Rationale

[More Information Needed]

### Source Data

[More Information Needed]

#### Initial Data Collection and Normalization

[More Information Needed]

#### Who are the source language producers?

[More Information Needed]

### Annotations

[More Information Needed]

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

Thanks to [@abhishekkrthakur](https://github.com/abhishekkrthakur) for adding this dataset.