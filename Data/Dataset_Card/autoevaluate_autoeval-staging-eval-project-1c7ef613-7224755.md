---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- ag_news
eval_info:
  task: multi_class_classification
  model: mrm8488/distilroberta-finetuned-age_news-classification
  dataset_name: ag_news
  dataset_config: default
  dataset_split: test
  col_mapping:
    text: text
    target: label
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Multi-class Text Classification
* Model: mrm8488/distilroberta-finetuned-age_news-classification
* Dataset: ag_news

To run new evaluation jobs, visit Hugging Face's [automatic evaluation service](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@abhishek](https://huggingface.co/abhishek) for evaluating this model.