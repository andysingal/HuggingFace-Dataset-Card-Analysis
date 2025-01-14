---
annotations_creators:
- crowdsourced
language_creators:
- crowdsourced
language:
- en
license:
- other
multilinguality:
- monolingual
pretty_name: multidogo
size_categories:
- 10k<n<100k
source_datasets:
- original
task_categories:
- text-classification
- sequence-modeling
- structure-prediction
- other
task_ids:
- intent-classification
- dialogue-modeling
- slot-filling
- named-entity-recognition
- other-other-my-task-description
---

MultiDoGo dialog dataset: 
- paper: https://aclanthology.org/D19-1460/
- git repo: https://github.com/awslabs/multi-domain-goal-oriented-dialogues-dataset

*Abstract*
The need for high-quality, large-scale, goal-oriented dialogue datasets continues to grow as virtual assistants become increasingly wide-spread. However, publicly available datasets useful for this area are limited either in their size, linguistic diversity, domain coverage, or annotation granularity. In this paper, we present strategies toward curating and annotating large scale goal oriented dialogue data. We introduce the MultiDoGO dataset to overcome these limitations. With a total of over 81K dialogues harvested across six domains, MultiDoGO is over 8 times the size of MultiWOZ, the other largest comparable dialogue dataset currently available to the public. Over 54K of these harvested conversations are annotated for intent classes and slot labels. We adopt a Wizard-of-Oz approach wherein a crowd-sourced worker (the “customer”) is paired with a trained annotator (the “agent”). The data curation process was controlled via biases to ensure a diversity in dialogue flows following variable dialogue policies. We provide distinct class label tags for agents vs. customer utterances, along with applicable slot labels. We also compare and contrast our strategies on annotation granularity, i.e. turn vs. sentence level. Furthermore, we compare and contrast annotations curated by leveraging professional annotators vs the crowd. We believe our strategies for eliciting and annotating such a dialogue dataset scales across modalities and domains and potentially languages in the future. To demonstrate the efficacy of our devised strategies we establish neural baselines for classification on the agent and customer utterances as well as slot labeling for each domain.

## Licensing information

Community Data License Agreement – Permissive, Version 1.0.