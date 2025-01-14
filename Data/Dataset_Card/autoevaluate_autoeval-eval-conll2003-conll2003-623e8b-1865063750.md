---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- conll2003
eval_info:
  task: entity_extraction
  model: dslim/bert-large-NER
  metrics: []
  dataset_name: conll2003
  dataset_config: conll2003
  dataset_split: test
  col_mapping:
    tokens: tokens
    tags: ner_tags
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Token Classification
* Model: dslim/bert-large-NER
* Dataset: conll2003
* Config: conll2003
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@rdecoupes](https://huggingface.co/rdecoupes) for evaluating this model.