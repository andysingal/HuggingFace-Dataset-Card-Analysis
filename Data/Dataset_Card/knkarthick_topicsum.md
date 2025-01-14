---
annotations_creators:
- expert-generated
language_creators:
- expert-generated
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
- summarization
- text2text-generation
- text-generation
task_ids: []
pretty_name: TopicSum Corpus
---
# Dataset Card for TopicSum Corpus [Single Dataset Comprising of XSUM & DialogSUM for One Liner Summarization/ Topic Generation of Text]
## Dataset Description
### Links
- **DialogSUM:** https://github.com/cylnlp/dialogsum
- **XSUM:** https://huggingface.co/datasets/knkarthick/xsum
- **Point of Contact:** https://huggingface.co/knkarthick

### Dataset Summary
TopicSUM is collection of large-scale dialogue summarization dataset from XSUM & DialogSUM, consisting of 241,171 dialogues with corresponding manually labeled one-liner summaries/ topics.
### Languages
English

## Dataset Structure
### Data Instances
TopicSum is a large-scale dialogue summarization dataset collection [XSUM & DialogDUM], consisting of 241,171 dialogues split into train, test and validation.

The first instance in the training set:
{'dialogue': 'The full cost of damage in Newton Stewart, one of the areas worst affected, is still being assessed.\nRepair work is ongoing in Hawick and many roads in Peeblesshire remain badly affected by standing water.\nTrains on the west coast mainline face disruption due to damage at the Lamington Viaduct.\nMany businesses and householders were affected by flooding in Newton Stewart after the River Cree overflowed into the town.\nFirst Minister Nicola Sturgeon visited the area to inspect the damage.\nThe waters breached a retaining wall, flooding many commercial properties on Victoria Street - the main shopping thoroughfare.\nJeanette Tate, who owns the Cinnamon Cafe which was badly affected, said she could not fault the multi-agency response once the flood hit.\nHowever, she said more preventative work could have been carried out to ensure the retaining wall did not fail.\n"It is difficult but I do think there is so much publicity for Dumfries and the Nith - and I totally appreciate that - but it is almost like we\'re neglected or forgotten," she said.\n"That may not be true but it is perhaps my perspective over the last few days.\n"Why were you not ready to help us a bit more when the warning and the alarm alerts had gone out?"\nMeanwhile, a flood alert remains in place across the Borders because of the constant rain.\nPeebles was badly hit by problems, sparking calls to introduce more defences in the area.\nScottish Borders Council has put a list on its website of the roads worst affected and drivers have been urged not to ignore closure signs.\nThe Labour Party\'s deputy Scottish leader Alex Rowley was in Hawick on Monday to see the situation first hand.\nHe said it was important to get the flood protection plan right but backed calls to speed up the process.\n"I was quite taken aback by the amount of damage that has been done," he said.\n"Obviously it is heart-breaking for people who have been forced out of their homes and the impact on businesses."\nHe said it was important that "immediate steps" were taken to protect the areas most vulnerable and a clear timetable put in place for flood prevention plans.\nHave you been affected by flooding in Dumfries and Galloway or the Borders? Tell us about your experience of the situation and how it was handled. Email us on selkirk.news@bbc.co.uk or dumfries@bbc.co.uk.', 'summary': 'Clean-up operations are continuing across the Scottish Borders and Dumfries and Galloway after flooding caused by Storm Frank.', 
'id': '35232142'}

### Data Fields
- dialogue: text of dialogue.
- summary: human written one-liner summary/ topic of the dialogue.
- id: unique file id of an example.

### Data Splits
- train: 216,505
- val: 11,832
- test: 12,834

## Dataset Creation
### Curation Rationale
Collection of XSUM & DialogSUM Datasets.
### Who are the source language producers?
linguists
### Who are the annotators?
language experts

## Licensing Information
non-commercial licence: MIT
## Citation Information
Refer the above links for Credits & Citations.