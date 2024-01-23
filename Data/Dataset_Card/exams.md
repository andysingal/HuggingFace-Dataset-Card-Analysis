---
pretty_name: EXAMS
annotations_creators:
- found
language_creators:
- found
language:
- ar
- bg
- de
- es
- fr
- hr
- hu
- it
- lt
- mk
- pl
- pt
- sq
- sr
- tr
- vi
license:
- cc-by-sa-4.0
multilinguality:
- monolingual
- multilingual
size_categories:
- 10K<n<100K
- 1K<n<10K
- n<1K
source_datasets:
- original
task_categories:
- question-answering
task_ids:
- multiple-choice-qa
paperswithcode_id: exams
configs:
- alignments
- crosslingual_bg
- crosslingual_hr
- crosslingual_hu
- crosslingual_it
- crosslingual_mk
- crosslingual_pl
- crosslingual_pt
- crosslingual_sq
- crosslingual_sr
- crosslingual_test
- crosslingual_tr
- crosslingual_vi
- crosslingual_with_para_bg
- crosslingual_with_para_hr
- crosslingual_with_para_hu
- crosslingual_with_para_it
- crosslingual_with_para_mk
- crosslingual_with_para_pl
- crosslingual_with_para_pt
- crosslingual_with_para_sq
- crosslingual_with_para_sr
- crosslingual_with_para_test
- crosslingual_with_para_tr
- crosslingual_with_para_vi
- multilingual
- multilingual_with_para
dataset_info:
- config_name: alignments
  features:
  - name: source_id
    dtype: string
  - name: target_id_list
    sequence: string
  splits:
  - name: full
    num_bytes: 1265280
    num_examples: 10834
  download_size: 169745177
  dataset_size: 1265280
- config_name: multilingual
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 3385865
    num_examples: 7961
  - name: validation
    num_bytes: 1143067
    num_examples: 2672
  - name: test
    num_bytes: 5753625
    num_examples: 13510
  download_size: 169745177
  dataset_size: 10282557
- config_name: multilingual_with_para
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 127298595
    num_examples: 7961
  - name: validation
    num_bytes: 42713069
    num_examples: 2672
  - name: test
    num_bytes: 207981218
    num_examples: 13510
  download_size: 169745177
  dataset_size: 377992882
- config_name: crosslingual_test
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: test
    num_bytes: 8412531
    num_examples: 19736
  download_size: 169745177
  dataset_size: 8412531
- config_name: crosslingual_with_para_test
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: test
    num_bytes: 207981218
    num_examples: 13510
  download_size: 169745177
  dataset_size: 207981218
- config_name: crosslingual_bg
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 1078545
    num_examples: 2344
  - name: validation
    num_bytes: 282115
    num_examples: 593
  download_size: 169745177
  dataset_size: 1360660
- config_name: crosslingual_with_para_bg
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 47068024
    num_examples: 2344
  - name: validation
    num_bytes: 11916370
    num_examples: 593
  download_size: 169745177
  dataset_size: 58984394
- config_name: crosslingual_hr
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 808320
    num_examples: 2341
  - name: validation
    num_bytes: 176910
    num_examples: 538
  download_size: 169745177
  dataset_size: 985230
- config_name: crosslingual_with_para_hr
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 24890820
    num_examples: 2341
  - name: validation
    num_bytes: 5695382
    num_examples: 538
  download_size: 169745177
  dataset_size: 30586202
- config_name: crosslingual_hu
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 678447
    num_examples: 1731
  - name: validation
    num_bytes: 202324
    num_examples: 536
  download_size: 169745177
  dataset_size: 880771
- config_name: crosslingual_with_para_hu
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 19036575
    num_examples: 1731
  - name: validation
    num_bytes: 6043577
    num_examples: 536
  download_size: 169745177
  dataset_size: 25080152
- config_name: crosslingual_it
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 399864
    num_examples: 1010
  - name: validation
    num_bytes: 93343
    num_examples: 246
  download_size: 169745177
  dataset_size: 493207
- config_name: crosslingual_with_para_it
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 16409787
    num_examples: 1010
  - name: validation
    num_bytes: 4018497
    num_examples: 246
  download_size: 169745177
  dataset_size: 20428284
- config_name: crosslingual_mk
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 826582
    num_examples: 1665
  - name: validation
    num_bytes: 204570
    num_examples: 410
  download_size: 169745177
  dataset_size: 1031152
- config_name: crosslingual_with_para_mk
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 38446774
    num_examples: 1665
  - name: validation
    num_bytes: 9673826
    num_examples: 410
  download_size: 169745177
  dataset_size: 48120600
- config_name: crosslingual_pl
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 574246
    num_examples: 1577
  - name: validation
    num_bytes: 141877
    num_examples: 394
  download_size: 169745177
  dataset_size: 716123
- config_name: crosslingual_with_para_pl
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 16374617
    num_examples: 1577
  - name: validation
    num_bytes: 4159076
    num_examples: 394
  download_size: 169745177
  dataset_size: 20533693
- config_name: crosslingual_pt
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 375214
    num_examples: 740
  - name: validation
    num_bytes: 87850
    num_examples: 184
  download_size: 169745177
  dataset_size: 463064
- config_name: crosslingual_with_para_pt
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 12185799
    num_examples: 740
  - name: validation
    num_bytes: 3093848
    num_examples: 184
  download_size: 169745177
  dataset_size: 15279647
- config_name: crosslingual_sq
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 424388
    num_examples: 1194
  - name: validation
    num_bytes: 110293
    num_examples: 311
  download_size: 169745177
  dataset_size: 534681
- config_name: crosslingual_with_para_sq
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 17341921
    num_examples: 1194
  - name: validation
    num_bytes: 4450152
    num_examples: 311
  download_size: 169745177
  dataset_size: 21792073
- config_name: crosslingual_sr
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 650268
    num_examples: 1323
  - name: validation
    num_bytes: 145928
    num_examples: 314
  download_size: 169745177
  dataset_size: 796196
- config_name: crosslingual_with_para_sr
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 24576553
    num_examples: 1323
  - name: validation
    num_bytes: 5772713
    num_examples: 314
  download_size: 169745177
  dataset_size: 30349266
- config_name: crosslingual_tr
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 718431
    num_examples: 1571
  - name: validation
    num_bytes: 182974
    num_examples: 393
  download_size: 169745177
  dataset_size: 901405
- config_name: crosslingual_with_para_tr
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 18597963
    num_examples: 1571
  - name: validation
    num_bytes: 4763341
    num_examples: 393
  download_size: 169745177
  dataset_size: 23361304
- config_name: crosslingual_vi
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 954191
    num_examples: 1955
  - name: validation
    num_bytes: 232264
    num_examples: 488
  download_size: 169745177
  dataset_size: 1186455
- config_name: crosslingual_with_para_vi
  features:
  - name: id
    dtype: string
  - name: question
    struct:
    - name: stem
      dtype: string
    - name: choices
      sequence:
      - name: text
        dtype: string
      - name: label
        dtype: string
      - name: para
        dtype: string
  - name: answerKey
    dtype: string
  - name: info
    struct:
    - name: grade
      dtype: int32
    - name: subject
      dtype: string
    - name: language
      dtype: string
  splits:
  - name: train
    num_bytes: 40884023
    num_examples: 1955
  - name: validation
    num_bytes: 10260662
    num_examples: 488
  download_size: 169745177
  dataset_size: 51144685
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

- **Repository:** https://github.com/mhardalov/exams-qa
- **Paper:** [EXAMS: A Multi-Subject High School Examinations Dataset for Cross-Lingual and Multilingual Question Answering](https://arxiv.org/abs/2011.03080)
- **Point of Contact:** [hardalov@@fmi.uni-sofia.bg](hardalov@@fmi.uni-sofia.bg)

### Dataset Summary

EXAMS is a benchmark dataset for multilingual and cross-lingual question answering from high school examinations. It consists of more than 24,000 high-quality high school exam questions in 16 languages, covering 8 language families and 24 school subjects from Natural Sciences and Social Sciences, among others.

### Supported Tasks and Leaderboards

[More Information Needed]

### Languages

The languages in the dataset are:
- ar
- bg
- de
- es
- fr
- hr
- hu
- it
- lt
- mk
- pl
- pt
- sq
- sr
- tr
- vi

## Dataset Structure

### Data Instances

An example of a data instance (with support paragraphs, in Bulgarian) is:
```
{'answerKey': 'C',
 'id': '35dd6b52-7e71-11ea-9eb1-54bef70b159e',
 'info': {'grade': 12, 'language': 'Bulgarian', 'subject': 'Biology'},
 'question': {'choices': {'label': ['A', 'B', 'C', 'D'],
   'para': ['Това води до наследствени изменения между организмите. Мирновременните вождове са наследствени. Черният, сивият и кафявият цвят на оцветяване на тялото се определя от пигмента меланин и възниква в резултат на наследствени изменения. Тези различия, според Монтескьо, не са наследствени. Те са и важни наследствени вещи в клана. Те са били наследствени архонти и управляват демократично. Реликвите са исторически, религиозни, семейни (наследствени) и технически. Общо са направени 800 изменения. Не всички наследствени аномалии на хемоглобина са вредни, т.е. Моногенните наследствени болести, които водят до мигрена, са редки. Няма наследствени владетели. Повечето от тях са наследствени и се предават на потомството. Всичките синове са ерцхерцози на всичките наследствени земи и претенденти. През 1509 г. Фраунбергите са издигнати на наследствени имперски графове. Фамилията Валдбург заради постиженията са номинирани на „наследствени имперски трушсеси“. Фамилията Валдбург заради постиженията са номинирани на „наследствени имперски трушсеси“. Описани са единични наследствени случаи, но по-често липсва фамилна обремененост. Позициите им са наследствени и се предават в рамките на клана. Внесени са изменения в конструкцията на веригите. и са направени изменения в ходовата част. На храма са правени лоши архитектурни изменения. Изменения са предприети и вътре в двореца. Имало двама наследствени вождове. Имало двама наследствени вождове. Годишният календар, „компасът“ и биологичния часовник са наследствени и при много бозайници.',
    'Постепенно задълбочаващите се функционални изменения довеждат и до структурни изменения. Те се дължат както на растягането на кожата, така и на въздействието на хормоналните изменения върху кожната тъкан. тези изменения се долавят по-ясно. Впоследствие, той претърпява изменения. Ширината остава без изменения. След тяхното издаване се налагат изменения в първоначалния Кодекс, защото не е съобразен с направените в Дигестите изменения. Еволюционният преход се характеризира със следните изменения: Наблюдават се и сезонни изменения в теглото. Приемат се изменения и допълнения към Устава. Тук се размножават и предизвикват възпалителни изменения. Общо са направени 800 изменения. Бронирането не претърпява съществени изменения. При животните се откриват изменения при злокачествената форма. Срещат се и дегенеративни изменения в семенните каналчета. ТАВКР „Баку“ се строи по изменения проект 1143.4. Трансът се съпровожда с определени изменения на мозъчната дейност. На изменения е подложен и Светия Синод. Внесени са изменения в конструкцията на веригите. На храма са правени лоши архитектурни изменения. Оттогава стиховете претърпяват изменения няколко пъти. Настъпват съществени изменения в музикалната култура. По-късно той претърпява леки изменения. Настъпват съществени изменения в музикалната култура. Претърпява сериозни изменения само носовата надстройка. Хоризонталното брониране е оставено без изменения.',
    'Модификациите са обратими. Тези реакции са обратими. В началните стадии тези натрупвания са обратими. Всички такива ефекти са временни и обратими. Много от реакциите са обратими и идентични с тези при гликолизата. Ако в обращение има книжни пари, те са обратими в злато при поискване . Общо са направени 800 изменения. Непоследователността е представена от принципа на "симетрия", при който взаимоотношенията са разглеждани като симетрични или обратими. Откакто формулите в клетките на електронната таблица не са обратими, тази техника е с ограничена стойност. Ефектът на Пелтие-Зеебек и ефектът Томсън са обратими (ефектът на Пелтие е обратен на ефекта на Зеебек). Плазмолизата протича в три етапа, в зависимост от силата и продължителността на въздействието:\n\nПървите два етапа са обратими. Внесени са изменения в конструкцията на веригите. и са направени изменения в ходовата част. На храма са правени лоши архитектурни изменения. Изменения са предприети и вътре в двореца. Оттогава насетне екипите не са претърпявали съществени изменения. Изменения са направени и в колесника на машината. Тези изменения са обявени през октомври 1878 година. Последните изменения са внесени през януари 2009 година. В процеса на последващото проектиране са внесени някои изменения. Сериозните изменения са в края на Втората световна война. Внесени са изменения в конструкцията на погребите и подемниците. Внесени са изменения в конструкцията на погребите и подемниците. Внесени са изменения в конструкцията на погребите и подемниците. Постепенно задълбочаващите се функционални изменения довеждат и до структурни изменения.',
    'Ерозионни процеси от масов характер липсват. Обновлението в редиците на партията приема масов характер. Тя обаче няма масов характер поради спецификата на формата. Движението против десятъка придобива масов характер и в Балчишка околия. Понякога екзекутирането на „обсебените от Сатана“ взимало невероятно масов характер. Укриването на дължими като наряд продукти в селата придобива масов характер. Периодичните миграции са в повечето случаи с масов характер и са свързани със сезонните изменения в природата, а непериодичните са премествания на животни, които настъпват след пожари, замърсяване на средата, висока численост и др. Имат необратим характер. Именно по време на двувековните походи на западните рицари използването на гербовете придобива масов характер. След присъединяването на Южен Кавказ към Русия, изселването на азербайджанци от Грузия придобива масов характер. Те имат нормативен характер. Те имат установителен характер. Освобождаването на работна сила обикновено има масов характер, защото обхваща големи контингенти от носителите на труд. Валежите имат подчертано континентален характер. Имат най-често издънков характер. Приливите имат предимно полуденонощен характер. Някои от тях имат мистериален характер. Тези сведения имат случаен, епизодичен характер. Те имат сезонен или годишен характер. Временните обезпечителни мерки имат временен характер. Други имат пожелателен характер (Здравко, Слава). Ловът и събирачеството имат спомагателен характер. Фактически успяват само малко да усилят бронирането на артилерийските погреби, другите изменения носят само частен характер. Някои карикатури имат само развлекателен характер, докато други имат политически нюанси. Поемите на Хезиод имат по-приложен характер.'],
   'text': ['дължат се на фенотипни изменения',
    'имат масов характер',
    'са наследствени',
    'са обратими']},
  'stem': 'Мутационите изменения:'}}
```

### Data Fields

A data instance contains the following fields:
- `id`: A question ID, unique across the dataset
- `question`: the question contains the following:
  - `stem`: a stemmed representation of the question textual
  - `choices`: a set of 3 to 5 candidate answers, which each have:
    - `text`: the text of the answers
    - `label`: a label in `['A', 'B', 'C', 'D', 'E']` used to match to the `answerKey`
    - `para`: (optional) a supported paragraph from Wikipedia in the same language as the question and answer
- `answerKey`: the key corresponding to the right answer's `label`
- `info`: some additional information on the question including:
  - `grade`: the school grade for the exam this question was taken from
  - `subject`: a free text description of the academic subject
  - `language`: the English name of the language for this question

### Data Splits

Depending on the configuration, the dataset have different splits:
- "alignments": a single "full" split
- "multilingual" and "multilingual_with_para": "train", "validation" and "test" splits
- "crosslingual_test" and "crosslingual_with_para_test": a single "test" split
- the rest of crosslingual configurations: "train" and "validation" splits

## Dataset Creation

### Curation Rationale

[More Information Needed]

### Source Data

#### Initial Data Collection and Normalization

Eχαµs was collected from official state exams prepared by the ministries of education of various countries. These exams are taken by students graduating from high school, and often require knowledge learned through the entire course.

The questions cover a large variety of subjects and material based on the country’s education system. They cover major school subjects such as Biology, Chemistry, Geography, History, and Physics, but we also  highly specialized ones such as Agriculture, Geology, Informatics, as well as some applied and profiled studies.

Some countries allow students to take official examinations in several languages. This dataset provides 9,857 parallel question pairs spread across seven languages coming from Croatia (Croatian, Serbian, Italian, Hungarian), Hungary (Hungarian, German, French, Spanish, Croatian, Serbian, Italian), and North Macedonia (Macedonian, Albanian, Turkish).

For all languages in the dataset, the first step in the process of data collection was to download the PDF files per year, per subject, and per language (when parallel languages were available in the same source), convert the PDF files to text, and select those that were well formatted and followed the document structure.

Then, Regular Expressions (RegEx) were used to parse the questions, their corresponding choices and the correct answer choice. In order to ensure that all our questions are answerable using textual input only, questions that contained visual information were removed, as selected by using curated list of words such as map, table, picture, graph, etc., in the corresponding language.

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

The dataset, which contains paragraphs from Wikipedia, is licensed under CC-BY-SA 4.0. The code in this repository is licensed according the [LICENSE file](https://raw.githubusercontent.com/mhardalov/exams-qa/main/LICENSE).

### Citation Information

```
@article{hardalov2020exams,
  title={EXAMS: A Multi-subject High School Examinations Dataset for Cross-lingual and Multilingual Question Answering},
  author={Hardalov, Momchil and Mihaylov, Todor and Dimitrina Zlatkova and Yoan Dinkov and Ivan Koychev and Preslav Nvakov},
  journal={arXiv preprint arXiv:2011.03080},
  year={2020}
}
```

### Contributions

Thanks to [@yjernite](https://github.com/yjernite) for adding this dataset.