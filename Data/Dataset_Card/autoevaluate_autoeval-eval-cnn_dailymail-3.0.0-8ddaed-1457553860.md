---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- cnn_dailymail
eval_info:
  task: summarization
  model: ARTeLab/it5-summarization-fanpage
  metrics: []
  dataset_name: cnn_dailymail
  dataset_config: 3.0.0
  dataset_split: train
  col_mapping:
    text: article
    target: highlights
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: ARTeLab/it5-summarization-fanpage
* Dataset: cnn_dailymail
* Config: 3.0.0
* Split: train

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@ehahaha](https://huggingface.co/ehahaha) for evaluating this model.