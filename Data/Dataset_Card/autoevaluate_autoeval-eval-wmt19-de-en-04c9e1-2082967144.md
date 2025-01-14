---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- wmt19
eval_info:
  task: translation
  model: facebook/wmt19-en-de
  metrics: []
  dataset_name: wmt19
  dataset_config: de-en
  dataset_split: validation
  col_mapping:
    source: translation.en
    target: translation.de
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Translation
* Model: facebook/wmt19-en-de
* Dataset: wmt19
* Config: de-en
* Split: validation

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@WillHeld](https://huggingface.co/WillHeld) for evaluating this model.