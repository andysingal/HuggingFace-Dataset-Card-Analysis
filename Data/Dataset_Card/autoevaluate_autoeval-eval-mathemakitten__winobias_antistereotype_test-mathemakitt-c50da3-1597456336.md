---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- mathemakitten/winobias_antistereotype_test
eval_info:
  task: text_zero_shot_classification
  model: facebook/opt-66b
  metrics: []
  dataset_name: mathemakitten/winobias_antistereotype_test
  dataset_config: mathemakitten--winobias_antistereotype_test
  dataset_split: test
  col_mapping:
    text: text
    classes: classes
    target: target
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Zero-Shot Text Classification
* Model: facebook/opt-66b
* Dataset: mathemakitten/winobias_antistereotype_test
* Config: mathemakitten--winobias_antistereotype_test
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@mathemakitten](https://huggingface.co/mathemakitten) for evaluating this model.