---
annotations_creators:
- found
language_creators:
- found
language:
- th
license:
- lgpl-3.0
multilinguality:
- monolingual
size_categories:
- 10K<n<100K
source_datasets:
- original
task_categories:
- text-classification
task_ids:
- sentiment-classification
pretty_name: WongnaiReviews
dataset_info:
  features:
  - name: review_body
    dtype: string
  - name: star_rating
    dtype:
      class_label:
        names:
          '0': '1'
          '1': '2'
          '2': '3'
          '3': '4'
          '4': '5'
  splits:
  - name: train
    num_bytes: 60691428
    num_examples: 40000
  - name: test
    num_bytes: 9913686
    num_examples: 6203
  download_size: 16556587
  dataset_size: 70605114
---

# Dataset Card for Wongnai_Reviews

## Dataset Description

- **Repository:** https://github.com/wongnai/wongnai-corpus

### Dataset Summary

The Wongnai Review dataset contains restaurant reviews and ratings, almost entirely in Thai language.

The reviews are in 5 classes ranging from 1 to 5 stars.

This dataset was featured in a Kaggle challenge https://www.kaggle.com/c/wongnai-challenge-review-rating-prediction/overview

### Languages

Thai

## Dataset Structure

### Data Fields

- review_body - text of review
- star_rating - an integer star rating (1-5) or -1 (for test)

### Data Splits

Designated train (40,000 reviews) and test (6,204) sets.

### Source Data

#### Initial Data Collection and Normalization

Data was collected by Wongnai from business reviews on their website,
and shared on GitHub and Kaggle.

### Annotations

The reviews are users' own star ratings, so no additional annotation was needed.

## Additional Information

### Dataset Curators

Contributors to original GitHub repo:
- Ekkalak Thongthanomkul
- Tanapol Nearunchorn
- Yuwat Chuesathuchon

### Licensing Information

LGPL-3.0

### Citation Information

See https://github.com/wongnai/wongnai-corpus

### Contributions

Thanks to [@mapmeld](https://github.com/mapmeld), [@cstorm125](https://github.com/cstorm125) for adding this dataset.