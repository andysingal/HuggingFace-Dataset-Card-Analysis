---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- phpthinh/ex3
eval_info:
  task: text_zero_shot_classification
  model: bigscience/bloom-560m
  metrics: []
  dataset_name: phpthinh/ex3
  dataset_config: all
  dataset_split: test
  col_mapping:
    text: text
    classes: classes
    target: target
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Zero-Shot Text Classification
* Model: bigscience/bloom-560m
* Dataset: phpthinh/ex3
* Config: all
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@phpthinh](https://huggingface.co/phpthinh) for evaluating this model.