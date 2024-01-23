---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- glue
eval_info:
  task: multi_class_classification
  model: JeremiahZ/bert-base-uncased-cola
  metrics: ['matthews_correlation']
  dataset_name: glue
  dataset_config: cola
  dataset_split: validation
  col_mapping:
    text: sentence
    target: label
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Multi-class Text Classification
* Model: JeremiahZ/bert-base-uncased-cola
* Dataset: glue
* Config: cola
* Split: validation

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@JeremiahZ](https://huggingface.co/JeremiahZ) for evaluating this model.