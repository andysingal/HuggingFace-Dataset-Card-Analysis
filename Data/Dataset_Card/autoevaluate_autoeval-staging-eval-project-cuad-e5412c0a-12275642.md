---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- cuad
eval_info:
  task: extractive_question_answering
  model: 21iridescent/RoBERTa-base-finetuned-squad2-lwt
  metrics: []
  dataset_name: cuad
  dataset_config: default
  dataset_split: test
  col_mapping:
    context: context
    question: question
    answers-text: answers.text
    answers-answer_start: answers.answer_start
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Question Answering
* Model: 21iridescent/RoBERTa-base-finetuned-squad2-lwt
* Dataset: cuad
* Config: default
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@halima](https://huggingface.co/halima) for evaluating this model.