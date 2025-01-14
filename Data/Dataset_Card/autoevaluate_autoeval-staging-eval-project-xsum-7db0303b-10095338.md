---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- xsum
eval_info:
  task: summarization
  model: philschmid/distilbart-cnn-12-6-samsum
  metrics: []
  dataset_name: xsum
  dataset_config: default
  dataset_split: test
  col_mapping:
    text: document
    target: summary
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: philschmid/distilbart-cnn-12-6-samsum
* Dataset: xsum

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@ArjunPrSarkhel](https://huggingface.co/ArjunPrSarkhel) for evaluating this model.