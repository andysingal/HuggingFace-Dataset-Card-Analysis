---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- SpaceDoge/dataset_test_1
eval_info:
  task: text_zero_shot_classification
  model: inverse-scaling/opt-1.3b_eval
  metrics: []
  dataset_name: SpaceDoge/dataset_test_1
  dataset_config: SpaceDoge--dataset_test_1
  dataset_split: test
  col_mapping:
    text: prompt
    classes: classes
    target: answer_index
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Zero-Shot Text Classification
* Model: inverse-scaling/opt-1.3b_eval
* Dataset: SpaceDoge/dataset_test_1
* Config: SpaceDoge--dataset_test_1
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@SpaceDoge](https://huggingface.co/SpaceDoge) for evaluating this model.