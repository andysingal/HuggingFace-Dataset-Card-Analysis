---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- cnn_dailymail
eval_info:
  task: summarization
  model: nbroad/longt5-base-global-mediasum
  metrics: []
  dataset_name: cnn_dailymail
  dataset_config: 3.0.0
  dataset_split: test
  col_mapping:
    text: article
    target: highlights
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: nbroad/longt5-base-global-mediasum
* Dataset: cnn_dailymail
* Config: 3.0.0
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@nbroad](https://huggingface.co/nbroad) for evaluating this model.