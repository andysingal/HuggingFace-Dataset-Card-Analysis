---
annotations_creators:
- found
language_creators:
- expert-generated
- found
language:
- en
- zh
license:
- unknown
multilinguality:
- monolingual
size_categories:
- 1K<n<10K
- n<1K
source_datasets:
- original
task_categories:
- question-answering
task_ids:
- closed-domain-qa
pretty_name: CovidQaUcsd
configs:
- en
- zh
dataset_info:
- config_name: en
  features:
  - name: dialogue_id
    dtype: int32
  - name: dialogue_url
    dtype: string
  - name: dialogue_turns
    sequence:
    - name: speaker
      dtype:
        class_label:
          names:
            '0': Patient
            '1': Doctor
    - name: utterance
      dtype: string
  splits:
  - name: train
    num_bytes: 484944
    num_examples: 572
  download_size: 0
  dataset_size: 484944
- config_name: zh
  features:
  - name: dialogue_id
    dtype: int32
  - name: dialogue_url
    dtype: string
  - name: dialogue_turns
    sequence:
    - name: speaker
      dtype:
        class_label:
          names:
            '0': 病人
            '1': 医生
    - name: utterance
      dtype: string
  splits:
  - name: train
    num_bytes: 1352377
    num_examples: 1088
  download_size: 0
  dataset_size: 1352377
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

- **Homepage:** https://github.com/UCSD-AI4H/COVID-Dialogue
- **Repository:** The data is also present in the same [GIT](https://github.com/UCSD-AI4H/COVID-Dialogue) repository
- **Paper:** https://pengtaoxie.github.io/coviddiag.pdf
- **Leaderboard:**
- **Point of Contact:**

### Dataset Summary

COVID-Dialogue-Dataset-English is an English medical dialogue dataset about COVID-19 and other types of pneumonia. Patients who are concerned that they may be infected by COVID-19 or other pneumonia consult doctors and doctors provide advice. There are 603 consultations.

COVID-Dialogue-Dataset-Chinese is a Chinese medical dialogue dataset about COVID-19 and other types of pneumonia. Patients who are concerned that they may be infected by COVID-19 or other pneumonia consult doctors and doctors provide advice. There are 1393 consultations.

The dataset is present as a single text file. COVID-Dialogue-Dataset-Chinese.txt for Chinese and COVID-Dialogue-Dataset-English.txt for English.

### Supported Tasks and Leaderboards

Used for QA tasks. There is also a COVID-19 dialogue generation model available for the Chinese Data. The pre-print and more information is available in [this arxiv pre-print](https://arxiv.org/abs/2005.05442).

### Languages

Monolingual. The datasets are in English (EN) and Chinese (ZH)

## Dataset Structure

### Data Instances

An example of dialogue is:

```
{
	'dialogue_id': 602, 
	'dialogue_url': 'https://www.healthtap.com/member/fg?page=/search/covid', 
	'dialogue_turns': [{'speaker': 'Patient', 
			    'utterance': 'Can coronavirus symptoms be mild for some people versus severe? For example, could it just involve being very fatigued, low grade fever for a few days and not the extreme symptoms? Or is it always a full blown cold and struggle to breathe?Can coronavirus symptoms be mild for some people versus severe? For example, could it just involve being very fatigued, low grade fever for a few days and not the extreme symptoms? Or is it always a full blown cold and struggle to breathe?'}, 
                           {'speaker': 'Doctor', 
                            'utterance': 'In brief:   Symptoms vary.   Some may have no symptoms at all. Some can be life threatening.   Would you like to video or text chat with me?'}]
}
```

The dataset is built from [icliniq.com](https://www.icliniq.com/), [healthcaremagic.com](https://www.healthcaremagic.com/), [healthtap.com](https://www.healthtap.com/) and all copyrights of the data belong to these websites. _(for English)_

The dataset is built from [Haodf.com](https://www.haodf.com/) and all copyrights of the data belong to [Haodf.com](https://www.haodf.com/).  _(for Chinese)_

### Data Fields

Each consultation consists of the below:
- ID
- URL
- Description of patient’s medical condition
- Dialogue
- Diagnosis and suggestions (Optional, mostly for Chinese)

For generating the QA only the below fields have been considered:
- ID : Consultatation Identifier (restarts for each file)
- URL: The url link of the extracted conversation
- Dialogue : The conversation between the doctor and the patient.

These are arranged as below in the prepared dataset. Each item will be represented with these parameters.

- "file_name": string - signifies the file from which the conversation was extracted
- "dialogue_id": int32 - the dialogue id
- "dialogue_url": string - url of the conversation
- "dialogue_turns": datasets.Sequence - sequence of dialogues between patient and the doctor.Consists ClassLabel(names=["病人", "医生"]), and "utterance"(string) for each turn. (ClassLable(names=["Patient", "Doctor"]) for english)

### Data Splits

There are no data splits on the original data

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

@article{ju2020CovidDialog,
  title={CovidDialog: Medical Dialogue Datasets about COVID-19},
  author={Ju, Zeqian and Chakravorty, Subrato and He, Xuehai and Chen, Shu and Yang, Xingyi and Xie, Pengtao},
  journal={ https://github.com/UCSD-AI4H/COVID-Dialogue}, 
  year={2020}
}

### Contributions

Thanks to [@vrindaprabhu](https://github.com/vrindaprabhu) for adding this dataset.