---
annotations_creators:
- no-annotation
language_creators:
- found
language:
- ar
- da
- de
- fi
- fr
- lb
- nl
- pt
license:
- cc0-1.0
multilinguality:
- multilingual
size_categories:
- 100K<n<1M
source_datasets:
- original
task_categories:
- text-generation
- fill-mask
task_ids:
- language-modeling
- masked-language-modeling
pretty_name: BnL Historical Newspapers
dataset_info:
  features:
  - name: id
    dtype: string
  - name: source
    dtype: string
  - name: url
    dtype: string
  - name: title
    dtype: string
  - name: ispartof
    dtype: string
  - name: text
    dtype: string
  - name: pub_date
    dtype: timestamp[s]
  - name: publisher
    dtype: string
  - name: language
    dtype: string
  - name: article_type
    dtype:
      class_label:
        names:
          '0': ADVERTISEMENT_SECTION
          '1': BIBLIOGRAPHY
          '2': CHAPTER
          '3': INDEX
          '4': CONTRIBUTION
          '5': TABLE_OF_CONTENTS
          '6': WEATHER
          '7': SHIPPING
          '8': SECTION
          '9': ARTICLE
          '10': TITLE_SECTION
          '11': DEATH_NOTICE
          '12': SUPPLEMENT
          '13': TABLE
          '14': ADVERTISEMENT
          '15': CHART_DIAGRAM
          '16': ILLUSTRATION
          '17': ISSUE
  - name: extent
    dtype: int32
  config_name: processed
  splits:
  - name: train
    num_bytes: 1611620156
    num_examples: 537558
  download_size: 1224029060
  dataset_size: 1611620156
---

# Dataset Card for BnL Historical Newspapers

## Table of Contents
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

- **Homepage:** https://data.bnl.lu/data/historical-newspapers/ 
- **Repository:**
- **Paper:**
- **Leaderboard:**
- **Point of Contact:** opendata@bnl.etat.lu

### Dataset Summary

The BnL has digitised over 800.000 pages of Luxembourg newspapers. This dataset currently has one configuration covering a subset of these newspapers, which sit under the "Processed Datasets" collection. The BNL:

> processed all newspapers and monographs that are in the public domain and extracted the full text and associated meta data of every single article, section, advertisement… The result is a large number of small, easy to use XML files formatted using Dublin Core.

[More Information Needed]

### Supported Tasks and Leaderboards

[More Information Needed]

### Languages

[More Information Needed]

## Dataset Structure

The dataset currently contains a single configuration.

### Data Instances

An example instance from the datasets:

``` python
{'id': 'https://persist.lu/ark:/70795/wx8r4c/articles/DTL47',
 'article_type': 8,
 'extent': 49,
 'ispartof': 'Luxemburger Wort',
 'pub_date': datetime.datetime(1853, 3, 23, 0, 0),
 'publisher': 'Verl. der St-Paulus-Druckerei',
 'source': 'newspaper/luxwort/1853-03-23',
 'text': 'Asien. Eine neue Nedcrland-Post ist angekommen mil Nachrichten aus Calcutta bis zum 5. Febr.; Vom» vay, 12. Febr. ; Nangun und HongKong, 13. Jan. Die durch die letzte Post gebrachle Nachricht, der König von Ava sei durch seinen Bruder enlhronl worden, wird bestätigt. (K. Z.) Verantwortl. Herausgeber, F. Schümann.',
 'title': 'Asien.',
 'url': 'http://www.eluxemburgensia.lu/webclient/DeliveryManager?pid=209701#panel:pp|issue:209701|article:DTL47',
 'language': 'de'
}
```


### Data Fields

- 'id': This is a unique and persistent identifier using ARK. 
- 'article_type': The type of the exported data, possible values ('ADVERTISEMENT_SECTION',
 'BIBLIOGRAPHY',
 'CHAPTER',
 'INDEX',
 'CONTRIBUTION',
 'TABLE_OF_CONTENTS',
 'WEATHER',
 'SHIPPING',
 'SECTION',
 'ARTICLE',
 'TITLE_SECTION',
 'DEATH_NOTICE',
 'SUPPLEMENT',
 'TABLE',
 'ADVERTISEMENT',
 'CHART_DIAGRAM',
 'ILLUSTRATION',
 'ISSUE')
- 'extent': The number of words in the text field
- 'ispartof: The complete title of the source document e.g. “Luxemburger Wort”.
- 'pub_date': The publishing date of the document e.g “1848-12-15”
- 'publisher':The publisher of the document e.g. “Verl. der St-Paulus-Druckerei”.
- 'source': Describes the source of the document. For example
<dc:source>newspaper/luxwort/1848-12-15</dc:source> means that this article comes from the newspaper “luxwort” (ID for Luxemburger Wort) issued on 15.12.1848.
- 'text': The full text of the entire article, section, advertisement etc. It includes any titles and subtitles as well. The content does not contain layout information, such as headings, paragraphs or lines.
- 'title': The main title of the article, section, advertisement, etc.
- 'url': The link to the BnLViewer on eluxemburgensia.lu to view the resource online.
- 'language': The language of the text, possible values ('ar', 'da', 'de', 'fi', 'fr', 'lb', 'nl', 'pt')

### Data Splits

This dataset contains a single split `train`.

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
@misc{bnl_newspapers,
title={Historical Newspapers},
url={https://data.bnl.lu/data/historical-newspapers/},
author={ Bibliothèque nationale du Luxembourg},
```

### Contributions

Thanks to [@davanstrien](https://github.com/davanstrien) for adding this dataset.