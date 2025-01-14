
---
annotations_creators:
- no-annotation
language:
- en
language_creators:
- other
license:
- cc-by-4.0
multilinguality:
- monolingual
pretty_name: COYO-700M
size_categories:
- 100M<n<1B
source_datasets:
- original
tags:
- image-text pairs
task_categories:
- text-to-image
- image-to-text
- zero-shot-classification
task_ids:
- image-captioning
---

# Dataset Card for COYO-700M

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

- **Homepage:** [COYO homepage](https://kakaobrain.com/contents/?contentId=7eca73e3-3089-43cb-b701-332e8a1743fd)
- **Repository:** [COYO repository](https://github.com/kakaobrain/coyo-dataset)
- **Paper:**
- **Leaderboard:**
- **Point of Contact:** [COYO email](coyo@kakaobrain.com)

### Dataset Summary

**COYO-700M** is a large-scale dataset that contains **747M image-text pairs** as well as many other **meta-attributes** to increase the usability to train various models. Our dataset follows a similar strategy to previous vision-and-language datasets, collecting many informative pairs of alt-text and its associated image in HTML documents. We expect COYO to be used to train popular large-scale foundation models 
complementary to other similar datasets. For more details on the data acquisition process, please refer to the technical paper to be released later.

### Supported Tasks and Leaderboards

We empirically validated the quality of COYO dataset by re-implementing popular models such as [ALIGN](https://arxiv.org/abs/2102.05918), [unCLIP](https://arxiv.org/abs/2204.06125), and [ViT](https://arxiv.org/abs/2010.11929). 
We trained these models on COYO-700M or its subsets from scratch, achieving competitive performance to the reported numbers or generated samples in the original papers. 
Our pre-trained models and training codes will be released soon along with the technical paper.

### Languages

The texts in the COYO-700M dataset consist of English.

## Dataset Structure

### Data Instances

Each instance in COYO-700M represents single image-text pair information with meta-attributes:
```
{
  'id': 841814333321,
  'url': 'https://blog.dogsof.com/wp-content/uploads/2021/03/Image-from-iOS-5-e1614711641382.jpg',
  'text': 'A Pomsky dog sitting and smiling in field of orange flowers',
  'width': 1000,
  'height': 988,
  'image_phash': 'c9b6a7d8469c1959',
  'text_length': 59,
  'word_count': 11,
  'num_tokens_bert': 13,
  'num_tokens_gpt': 12,
  'num_faces': 0,
  'clip_similarity_vitb32': 0.4296875,
  'clip_similarity_vitl14': 0.35205078125,
  'nsfw_score_opennsfw2': 0.00031447410583496094,
  'nsfw_score_gantman': 0.03298913687467575,
  'watermark_score': 0.1014641746878624,
  'aesthetic_score_laion_v2': 5.435476303100586
}
```

### Data Fields

| name                     | type    | description                                                                                                                                                                                |
|--------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| id                       | long    | Unique 64-bit integer ID generated by [monotonically_increasing_id()](https://spark.apache.org/docs/3.1.3/api/python/reference/api/pyspark.sql.functions.monotonically_increasing_id.html) |
| url                      | string  | The image URL extracted from the `src` attribute of the `<img>` tag                                                                                                                        |
| text                     | string  | The text extracted from the `alt` attribute of the `<img>` tag                                                                                                                             |
| width                    | integer | The width of the image                                                                                                                                                                     |
| height                   | integer | The height of the image                                                                                                                                                                    | 
| image_phash              | string  | The [perceptual hash(pHash)](http://www.phash.org/) of the image                                                                                                                           |
| text_length              | integer | The length of the text                                                                                                                                                                     |
| word_count               | integer | The number of words separated by spaces.                                                                                                                                                   |
| num_tokens_bert          | integer | The number of tokens using [BertTokenizer](https://huggingface.co/docs/transformers/model_doc/bert#transformers.BertTokenizer)                                                             |
| num_tokens_gpt           | integer | The number of tokens using [GPT2TokenizerFast](https://huggingface.co/docs/transformers/model_doc/gpt2#transformers.GPT2TokenizerFast)                                                     |
| num_faces                | integer | The number of faces in the image detected by [SCRFD](https://insightface.ai/scrfd)                                                                                                         |
| clip_similarity_vitb32   | float   | The cosine similarity between text and image(ViT-B/32) embeddings by [OpenAI CLIP](https://github.com/openai/CLIP)                                                                         |
| clip_similarity_vitl14   | float   | The cosine similarity between text and image(ViT-L/14) embeddings by [OpenAI CLIP](https://github.com/openai/CLIP)                                                                         |
| nsfw_score_opennsfw2     | float   | The NSFW score of the image by [OpenNSFW2](https://github.com/bhky/opennsfw2)                                                                                                              |
| nsfw_score_gantman       | float   | The NSFW score of the image by [GantMan/NSFW](https://github.com/GantMan/nsfw_model)                                                                                                       | 
| watermark_score          | float   | The watermark probability of the image by our internal model                                                                                                                               |
| aesthetic_score_laion_v2 | float   | The aesthetic score of the image by [LAION-Aesthetics-Predictor-V2](https://github.com/christophschuhmann/improved-aesthetic-predictor)                                                    |

### Data Splits

Data was not split, since the evaluation was expected to be performed on more widely used downstream task(s).

## Dataset Creation

### Curation Rationale

Similar to most vision-and-language datasets, our primary goal in the data creation process is to collect many pairs of alt-text and image sources in HTML documents crawled from the web. Therefore, We attempted to eliminate uninformative images or texts with minimal cost and improve our dataset's usability by adding various meta-attributes. Users can use these meta-attributes to sample a subset from COYO-700M and use it to train the desired model. For instance, the *num_faces* attribute could be used to make a subset like *COYO-Faces* and develop a privacy-preserving generative model.

### Source Data

#### Initial Data Collection and Normalization

We collected about 10 billion pairs of alt-text and image sources in HTML documents in [CommonCrawl](https://commoncrawl.org/) from Oct. 2020 to Aug. 2021. and eliminated uninformative pairs through the image and/or text level filtering process with minimal cost.

**Image Level**
* Included all image formats that [Pillow library](https://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html) can decode. (JPEG, WEBP, PNG, BMP, ...)
* Removed images less than 5KB image size.
* Removed images with an aspect ratio greater than 3.0.
* Removed images with min(width, height) < 200.
* Removed images with a score of [OpenNSFW2](https://github.com/bhky/opennsfw2) or [GantMan/NSFW](https://github.com/GantMan/nsfw_model) higher than 0.5.
* Removed all duplicate images based on the image [pHash](http://www.phash.org/) value from external public datasets.
    * ImageNet-1K/21K, Flickr-30K, MS-COCO, CC-3M, CC-12M

**Text Level**
* Collected only English text using [cld3](https://github.com/google/cld3).
* Replaced consecutive whitespace characters with a single whitespace and removed the whitespace before and after the sentence.
  (e.g. `"\n            \n                Load image into Gallery viewer, valentine&amp;#39;s day roses\n            \n" → "Load image into Gallery viewer, valentine&amp;#39;s day roses"`)
* Removed texts with a length of 5 or less.
* Removed texts that do not have a noun form.
* Removed texts with less than 3 words or more than 256 words and texts over 1000 in length.
* Removed texts appearing more than 10 times.
  (e.g. `“thumbnail for”, “image for”, “picture of”`)
* Removed texts containing NSFW words collected from [profanity_filter](https://github.com/rominf/profanity-filter/blob/master/profanity_filter/data/en_profane_words.txt), [better_profanity](https://github.com/snguyenthanh/better_profanity/blob/master/better_profanity/profanity_wordlist.txt), and [google_twunter_lol](https://gist.github.com/ryanlewis/a37739d710ccdb4b406d).

**Image-Text Level**
* Removed duplicated samples based on (image_phash, text).
  (Different text may exist for the same image URL.)

#### Who are the source language producers?

[Common Crawl](https://commoncrawl.org/) is the data source for COYO-700M.

### Annotations

#### Annotation process

The dataset was built in a fully automated process that did not require human annotation.

#### Who are the annotators?

No human annotation

### Personal and Sensitive Information

#### Disclaimer & Content Warning

The COYO dataset is recommended to be used for research purposes. 
Kakao Brain tried to construct a "Safe" dataset when building the COYO dataset. (See [Data Filtering](#source-data) Section) Kakao Brain is constantly making efforts to create more "Safe" datasets. 
However, despite these efforts, this large-scale dataset was not hand-picked by humans to avoid the risk due to its very large size (over 700M). 
Keep in mind that the unscreened nature of the dataset means that the collected images can lead to strongly discomforting and disturbing content for humans. 
The COYO dataset may contain some inappropriate data, and any problems resulting from such data are the full responsibility of the user who used it. 
Therefore, it is strongly recommended that this dataset be used only for research, keeping this in mind when using the dataset, and Kakao Brain does not recommend using this dataset as it is without special processing to clear inappropriate data to create commercial products.

## Considerations for Using the Data

### Social Impact of Dataset

It will be described in a paper to be released soon.

### Discussion of Biases

It will be described in a paper to be released soon.

### Other Known Limitations

It will be described in a paper to be released soon.

## Additional Information

### Dataset Curators

COYO dataset was released as an open source in the hope that it will be helpful to many research institutes and startups for research purposes. We look forward to contacting us from various places who wish to cooperate with us.

[coyo@kakaobrain.com](mailto:coyo@kakaobrain.com)

### Licensing Information

#### License

The COYO dataset of Kakao Brain is licensed under [CC-BY-4.0 License](https://creativecommons.org/licenses/by/4.0/).
The full license can be found in the [LICENSE.cc-by-4.0 file](./coyo-700m/blob/main/LICENSE.cc-by-4.0).
The dataset includes “Image URL” and “Text” collected from various sites by analyzing Common Crawl data, an open data web crawling project. 
The collected data (images and text) is subject to the license to which each content belongs.

#### Obligation to use

While Open Source may be free to use, that does not mean it is free of obligation. 
To determine whether your intended use of the COYO dataset is suitable for the CC-BY-4.0 license, please consider the license guide. 
If you violate the license, you may be subject to legal action such as the prohibition of use or claim for damages depending on the use.

### Citation Information

If you apply this dataset to any project and research, please cite our code:

```
@misc{kakaobrain2022coyo-700m,
  title         = {COYO-700M: Image-Text Pair Dataset},
  author        = {Minwoo Byeon, Beomhee Park, Haecheon Kim, Sungjun Lee, Woonhyuk Baek, Saehoon Kim},
  year          = {2022},
  howpublished  = {\url{https://github.com/kakaobrain/coyo-dataset}},
}
```

### Contributions

  - Minwoo Byeon ([@mwbyeon](https://github.com/mwbyeon))
  - Beomhee Park ([@beomheepark](https://github.com/beomheepark))
  - Haecheon Kim ([@HaecheonKim](https://github.com/HaecheonKim))
  - Sungjun Lee ([@justhungryman](https://github.com/justHungryMan))
  - Woonhyuk Baek ([@wbaek](https://github.com/wbaek))
  - Saehoon Kim ([@saehoonkim](https://github.com/saehoonkim))
  - and Kakao Brain Large-Scale AI Studio
