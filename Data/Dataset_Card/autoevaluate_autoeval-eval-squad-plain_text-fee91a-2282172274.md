---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- squad
eval_info:
  task: extractive_question_answering
  model: Aiyshwariya/bert-finetuned-squad
  metrics: ['squad', 'squad_v2']
  dataset_name: squad
  dataset_config: plain_text
  dataset_split: validation
  col_mapping:
    context: context
    question: question
    answers-text: answers.text
    answers-answer_start: answers.answer_start
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Question Answering
* Model: Aiyshwariya/bert-finetuned-squad
* Dataset: squad
* Config: plain_text
* Split: validation

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@bestuh](https://huggingface.co/bestuh) for evaluating this model.