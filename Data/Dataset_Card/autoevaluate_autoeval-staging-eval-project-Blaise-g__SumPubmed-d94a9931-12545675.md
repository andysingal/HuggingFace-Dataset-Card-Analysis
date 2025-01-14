---
type: predictions
tags:
- autotrain
- evaluation
datasets:
- Blaise-g/SumPubmed
eval_info:
  task: summarization
  model: Jacobsith/autotrain-Hello_there-1209845735
  metrics: []
  dataset_name: Blaise-g/SumPubmed
  dataset_config: Blaise-g--SumPubmed
  dataset_split: test
  col_mapping:
    text: text
    target: abstract
---
# Dataset Card for AutoTrain Evaluator

This repository contains model predictions generated by [AutoTrain](https://huggingface.co/autotrain) for the following task and dataset:

* Task: Summarization
* Model: Jacobsith/autotrain-Hello_there-1209845735
* Dataset: Blaise-g/SumPubmed
* Config: Blaise-g--SumPubmed
* Split: test

To run new evaluation jobs, visit Hugging Face's [automatic model evaluator](https://huggingface.co/spaces/autoevaluate/model-evaluator).

## Contributions

Thanks to [@Jacobsith](https://huggingface.co/Jacobsith) for evaluating this model.