---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- ml6team/cnn_dailymail_nl
eval_info:
  task: summarization
  model: yhavinga/t5-v1.1-large-dutch-cnn-test
  metrics: []
  dataset_name: ml6team/cnn_dailymail_nl
  dataset_config: default
  dataset_split: test
  col_mapping:
    text: article
    target: highlights
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: yhavinga/t5-v1.1-large-dutch-cnn-test
* Dataset: ml6team/cnn_dailymail_nl
* Config: default
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@yhavinga](https://huggingface.co/yhavinga) for evaluating this model.