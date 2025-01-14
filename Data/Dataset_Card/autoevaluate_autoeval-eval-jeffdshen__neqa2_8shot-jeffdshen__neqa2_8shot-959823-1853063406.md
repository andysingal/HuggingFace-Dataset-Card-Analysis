---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- jeffdshen/neqa2_8shot
eval_info:
  task: text_zero_shot_classification
  model: inverse-scaling/opt-66b_eval
  metrics: []
  dataset_name: jeffdshen/neqa2_8shot
  dataset_config: jeffdshen--neqa2_8shot
  dataset_split: train
  col_mapping:
    text: prompt
    classes: classes
    target: answer_index
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Zero-Shot Text Classification
* Model: inverse-scaling/opt-66b_eval
* Dataset: jeffdshen/neqa2_8shot
* Config: jeffdshen--neqa2_8shot
* Split: train

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@jeffdshen](https://huggingface.co/jeffdshen) for evaluating this model.