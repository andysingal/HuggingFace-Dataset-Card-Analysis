---
annotations_creators:
- expert-generated
language_creators:
- crowdsourced
language:
- en
license:
- mit
multilinguality:
- monolingual
size_categories:
- 100K<n<1M
source_datasets:
- original
task_categories:
- question-answering
- summarization
- text-retrieval
- text-generation
task_ids:
- abstractive-qa
- document-retrieval
- extractive-qa
pretty_name: 'DebateSum: A large-scale argument mining and summarization dataset'
language_bcp47:
- en-US
tags:
- conditional-text-generation
---

# DebateSum
Corresponding code repo for the upcoming paper at ARGMIN 2020: "DebateSum: A large-scale argument mining and summarization dataset"

Arxiv pre-print available here: https://arxiv.org/abs/2011.07251

Check out the presentation date and time here: https://argmining2020.i3s.unice.fr/node/9

Full paper as presented by the ACL is here: https://www.aclweb.org/anthology/2020.argmining-1.1/

Video of presentation at COLING 2020: https://underline.io/lecture/6461-debatesum-a-large-scale-argument-mining-and-summarization-dataset

The dataset is distributed as csv files. 

A search engine over DebateSum (as well as some additional evidence not included in DebateSum) is available as [debate.cards](http://debate.cards/). It's very good quality and allows for the evidence to be viewed in the format that debaters use. 

# Data 

DebateSum consists of **187328** debate documents, arguements (also can be thought of as abstractive summaries, or queries), word-level extractive summaries, citations, and associated metadata organized by topic-year. This data is ready for analysis by NLP systems.

## Download
All data is accesable in a parsed format organized by topic year [here](https://mega.nz/folder/ZdQGmK6b#-0hoBWc5fLYuxQuH25feXg)

Addtionally, the trained word-vectors for [debate2vec](https://github.com/Hellisotherpeople/debate2vec) are also found in that folder. 

## Regenerating it yourself 

This is useful as the debaters who produce the evidence release their work every year. Soon enough I will update to include the 2020-2021 topic. 

*Step 1: Download all open evidence files from [Open Evidence](https://openev.debatecoaches.org/) and unzip them into a directory. The links are as follows:*

* [2019](https://s3.amazonaws.com/openev/2019OpenEv.zip)    - Resolved: The United States federal government should substantially reduce Direct Commercial Sales and/or Foreign Military Sales of arms from the United States.
* [2018](https://s3.amazonaws.com/openev/2018OpenEv.zip)    - Resolved: The United States federal government should substantially reduce its restrictions on legal immigration to the United States.
* [2017](https://s3.amazonaws.com/openev/2017OpenEv.zip)    - Resolved: The United States federal government should substantially increase its funding and/or regulation of elementary and/or secondary education in the United States.
* [2016](https://s3.amazonaws.com/openev/2016OpenEv.zip)    - Resolved: The United States federal government should substantially increase its economic and/or diplomatic engagement with the People’s Republic of China.
* [2015](https://s3.amazonaws.com/openev/2015OpenEv.zip)    - Resolved: The United States federal government should substantially curtail its domestic surveil-lance.
* [2014](https://s3.amazonaws.com/openev/2014OpenEv.zip)    - Resolved: The United States federal government should substantially increase its non-military exploration and/or development of the Earth’s oceans.
* [2013](https://s3.amazonaws.com/openev/2013OpenEv.zip)    - Resolved: The United States federal government should substantially increase its economic en-gagement toward Cuba, Mexico or Venezuela.


*Step 2: Convert all evidence from docx files to html5 files using [pandoc](https://pandoc.org/) with this command:*
```
for f in *.docx; do pandoc "$f" -s -o "${f%.docx}.html5"; done
```

*Step 3: install the dependencies for make_debate_dataset.py.*

```
pip install -r requirements.txt
```

*Step 4: Modify the folder and file locations as needed for your system, and run make_debate_dataset.py*

```
python3 make_debate_dataset.py
```

# Credits 
Huge thanks to [Arvind Balaji](https://github.com/arvind-balaji) for making debate.cards and being second author on this paper! 
