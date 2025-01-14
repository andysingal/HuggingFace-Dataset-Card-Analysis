---
annotations_creators: []
language:
- es
language_creators: []
license:
- cc-by-nc-4.0
multilinguality:
- monolingual
pretty_name: Spanish Golden-Age Sonnets
size_categories: []
source_datasets: []
tags: []
task_categories: []
task_ids: []
---
[![DOI](https://zenodo.org/badge/46981468.svg)](https://zenodo.org/badge/latestdoi/46981468)

# Corpus of Spanish Golden-Age Sonnets

## Introduction
This corpus comprises sonnets written in Spanish between the 16th and 17th centuries.

This corpus is a dataset saved in .csv, from a previous one in .xml. 
All the information of the original dataset can be consulted in [its original repository](https://github.com/bncolorado/CorpusSonetosSigloDeOro).


Each sonnet has been annotated in accordance with the TEI standard. Besides the header and structural information, each sonnet includes the formal representation of each verse’s particular **metrical pattern**.

The pattern consists of a sequence of unstressed syllables (represented by the "-" sign) and stressed syllables ("+" sign). Thus, each verse’s metrical pattern is represented as follows:

	"---+---+-+-"
	
Each line in the metric_pattern codifies a line in the sonnet_text column.

## Column description
- 'author' (string): Author of the sonnet described
- 'sonnet_title' (string): Sonnet title
- 'sonnet_text' (string): Full text of the specific sonnet, divided by lines ('\n')
- 'metric_pattern' (string): Full metric pattern of the sonnet, in text, with TEI standard, divided by lines ('\n')
- 'reference_id' (int): Id of the original XML file where the sonnet is extracted
- 'publisher' (string): Name of the publisher
- 'editor' (string): Name of the editor
- 'research_author' (string): Name of the principal research author
- 'metrical_patterns_annotator' (string): Name of the annotation's checker
- 'research_group' (string): Name of the research group that processed the sonnet



## Poets
With the purpose of having a corpus as representative as possible, every author from the 16th and 17th centuries with more than 10 digitalized and available sonnets has been included.

All texts have been taken from the [Biblioteca Virtual Miguel de Cervantes](http://www.cervantesvirtual.com/).

Currently, the corpus comprises more than 5,000 sonnets (more than 71,000 verses).

## Annotation
The metrical pattern annotation has been carried out in a semi-automatic way. Firstly, all sonnets have been processed by an automatic metrical scansion system which assigns a distinct metrical pattern to each verse. Secondly, a part of the corpus has been manually checked and errors have been corrected.

Currently the corpus is going through the manual validation phase, and each sonnet includes information about whether it has already been manually checked or not.


## How to cite this corpus
If you would like to cite this corpus for academic research purposes, please use this reference:

Navarro-Colorado, Borja; Ribes Lafoz, María, and Sánchez, Noelia (2015) "Metrical annotation of a large corpus of Spanish sonnets: representation, scansion and evaluation" 10th edition of the Language Resources and Evaluation Conference 2016 Portorož, Slovenia. ([PDF](http://www.dlsi.ua.es/~borja/navarro2016_MetricalPatternsBank.pdf))

## Further Information
This corpus is part of the [ADSO project](https://adsoen.wordpress.com/), developed at the [University of Alicante](http://www.ua.es) and funded by [Fundación BBVA](http://www.fbbva.es/TLFU/tlfu/ing/home/index.jsp).

If you require further information about the metrical annotation, please consult the [Annotation Guide](https://github.com/bncolorado/CorpusSonetosSigloDeOro/blob/master/GuiaAnotacionMetrica.pdf) (in Spanish) or the following papers:

- Navarro-Colorado, Borja; Ribes-Lafoz, María and Sánchez, Noelia (2016) "Metrical Annotation of a Large Corpus of Spanish Sonnets: Representation, Scansion and Evaluation" [Proceedings of the Tenth International Conference on Language Resources and Evaluation (LREC 2016)](http://www.lrec-conf.org/proceedings/lrec2016/pdf/453_Paper.pdf) Portorož, Slovenia.

- Navarro-Colorado, Borja (2015) "A computational linguistic approach to Spanish Golden Age Sonnets: metrical and semantic aspects" [Computational Linguistics for Literature NAACL 2015](https://sites.google.com/site/clfl2015/), Denver (Co), USA ([PDF](https://aclweb.org/anthology/W/W15/W15-0712.pdf)).

## License
The metrical annotation of this corpus is licensed under a Creative Commons Attribution-Non Commercial 4.0 International License.

About the texts, "this digital object is protected by copyright and/or related rights. This digital object is accessible without charge, but its use is subject to the licensing conditions set by the organization giving access to it. Further information available at http://www.cervantesvirtual.com/marco-legal/ ".