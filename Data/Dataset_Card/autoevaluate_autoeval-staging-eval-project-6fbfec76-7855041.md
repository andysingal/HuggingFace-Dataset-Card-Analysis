---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- samsum
eval_info:
  task: summarization
  model: knkarthick/bart-large-xsum-samsum
  metrics: []
  dataset_name: samsum
  dataset_config: samsum
  dataset_split: test
  col_mapping:
    text: dialogue
    target: summary
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: knkarthick/bart-large-xsum-samsum
* Dataset: samsum

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@lewtun](https://huggingface.co/lewtun) for evaluating this model.