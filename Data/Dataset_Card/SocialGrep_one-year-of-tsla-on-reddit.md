---
annotations_creators:
- lexyr
language_creators:
- crowdsourced
language:
- en
license:
- cc-by-4.0
multilinguality:
- monolingual
size_categories:
- 100K<n<1M
source_datasets:
- original
---

# Dataset Card for one-year-of-tsla-on-reddit

## Table of Contents
- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
  - [Supported Tasks and Leaderboards](#supported-tasks-and-leaderboards)
  - [Languages](#languages)
- [Dataset Structure](#dataset-structure)
  - [Data Instances](#data-instances)
  - [Data Fields](#data-fields)
  - [Data Splits](#data-splits)
- [Dataset Creation](#dataset-creation)
  - [Curation Rationale](#curation-rationale)
  - [Source Data](#source-data)
  - [Annotations](#annotations)
  - [Personal and Sensitive Information](#personal-and-sensitive-information)
- [Considerations for Using the Data](#considerations-for-using-the-data)
  - [Social Impact of Dataset](#social-impact-of-dataset)
  - [Discussion of Biases](#discussion-of-biases)
  - [Other Known Limitations](#other-known-limitations)
- [Additional Information](#additional-information)
  - [Licensing Information](#licensing-information)

## Dataset Description

- **Homepage:** [https://socialgrep.com/datasets](https://socialgrep.com/datasets/one-year-of-tsla-on-reddit?utm_source=huggingface&utm_medium=link&utm_campaign=oneyearoftslaonreddit)
- **Reddit downloader used:** [https://socialgrep.com/exports](https://socialgrep.com/exports?utm_source=huggingface&utm_medium=link&utm_campaign=oneyearoftslaonreddit)
- **Point of Contact:** [Website](https://socialgrep.com/contact?utm_source=huggingface&utm_medium=link&utm_campaign=oneyearoftslaonreddit)

### Dataset Summary

A year's worth of mentions of Tesla Inc. (TSLA) in Reddit posts and comments.


### Languages

Mainly English.

## Dataset Structure

### Data Instances

A data point is a post or a comment. Due to the separate nature of the two, those exist in two different files - even though many fields are shared.

### Data Fields

- 'type': the type of the data point. Can be 'post' or 'comment'.
- 'id': the base-36 Reddit ID of the data point. Unique when combined with type.
- 'subreddit.id': the base-36 Reddit ID of the data point's host subreddit. Unique.
- 'subreddit.name': the human-readable name of the data point's host subreddit.
- 'subreddit.nsfw': a boolean marking the data point's host subreddit as NSFW or not.
- 'created_utc': a UTC timestamp for the data point.
- 'permalink': a reference link to the data point on Reddit.
- 'score': score of the data point on Reddit.

- 'domain': (Post only) the domain of the data point's link.
- 'url': (Post only) the destination of the data point's link, if any.
- 'selftext': (Post only) the self-text of the data point, if any.
- 'title': (Post only) the title of the post data point.

- 'body': (Comment only) the body of the comment data point.
- 'sentiment': (Comment only) the result of an in-house sentiment analysis pipeline. Used for exploratory analysis.

## Additional Information

### Licensing Information

CC-BY v4.0
