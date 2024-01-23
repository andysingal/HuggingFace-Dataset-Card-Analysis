---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- big_patent
eval_info:
  task: summarization
  model: google/bigbird-pegasus-large-bigpatent
  metrics: ['rouge']
  dataset_name: big_patent
  dataset_config: all
  dataset_split: validation
  col_mapping:
    text: description
    target: abstract
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: google/bigbird-pegasus-large-bigpatent
* Dataset: big_patent

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@kayvane](https://huggingface.co/kayvane) for evaluating this model.