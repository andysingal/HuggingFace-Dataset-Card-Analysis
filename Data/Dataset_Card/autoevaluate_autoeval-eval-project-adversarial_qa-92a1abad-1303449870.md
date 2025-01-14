---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- adversarial_qa
eval_info:
  task: extractive_question_answering
  model: nbroad/rob-base-superqa2
  metrics: []
  dataset_name: adversarial_qa
  dataset_config: adversarialQA
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
* Model: nbroad/rob-base-superqa2
* Dataset: adversarial_qa
* Config: adversarialQA
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@nbroad](https://huggingface.co/nbroad) for evaluating this model.