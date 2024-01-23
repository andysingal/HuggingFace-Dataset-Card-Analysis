---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- scan
eval_info:
  task: summarization
  model: ARTeLab/it5-summarization-fanpage
  metrics: []
  dataset_name: scan
  dataset_config: simple
  dataset_split: train
  col_mapping:
    text: commands
    target: actions
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: ARTeLab/it5-summarization-fanpage
* Dataset: scan
* Config: simple
* Split: train

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@test_yoon_0921](https://huggingface.co/test_yoon_0921) for evaluating this model.