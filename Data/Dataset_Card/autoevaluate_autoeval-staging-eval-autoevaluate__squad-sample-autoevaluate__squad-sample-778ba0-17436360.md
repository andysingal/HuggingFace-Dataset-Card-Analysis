---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- autoevaluate/squad-sample
eval_info:
  task: extractive_question_answering
  model: autoevaluate/extractive-question-answering-not-evaluated
  metrics: []
  dataset_name: autoevaluate/squad-sample
  dataset_config: autoevaluate--squad-sample
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
* Model: autoevaluate/extractive-question-answering-not-evaluated
* Dataset: autoevaluate/squad-sample
* Config: autoevaluate--squad-sample
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@lewtun](https://huggingface.co/lewtun) for evaluating this model.