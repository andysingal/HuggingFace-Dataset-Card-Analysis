---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- samsum
eval_info:
  task: summarization
  model: facebook/bart-large-cnn
  metrics: []
  dataset_name: samsum
  dataset_config: samsum
  dataset_split: validation
  col_mapping:
    text: dialogue
    target: summary
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: facebook/bart-large-cnn
* Dataset: samsum
* Config: samsum
* Split: validation

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@SamuelAllen1234](https://huggingface.co/SamuelAllen1234) for evaluating this model.