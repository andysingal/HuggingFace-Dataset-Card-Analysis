---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- futin/guess
eval_info:
  task: text_zero_shot_classification
  model: bigscience/bloom-1b7
  metrics: []
  dataset_name: futin/guess
  dataset_config: en_3
  dataset_split: test
  col_mapping:
    text: text
    classes: classes
    target: target
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Zero-Shot Text Classification
* Model: bigscience/bloom-1b7
* Dataset: futin/guess
* Config: en_3
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@futin](https://huggingface.co/futin) for evaluating this model.