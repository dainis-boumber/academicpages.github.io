---
layout: archive
title: "Datasets"
permalink: /datasets/
author_profile: true
redirect_from:
  - /data
---

{% include base_path %}

As part of our work, research, and publications, we designed and mined a number of datasets. Here I make available to the public datasets that had been peer reviewed, and novel but (in my opinion) high quality ones to be used in future work.
[Known as MLP-400 because of being based on 400 scientific publications by top authors by citations in machine learning, they are available here.](https://github.com/dainis-boumber/MLP-400-datasets)
MLPA-400 is a multiclass, mutilable authorship attribution problem. See it's own README.md and Weka for details
MLP-400AV is a new flexible dataset that uses the same data but for Authrship Verification. Because of it's extensive API, it can be adapted to almost any NLP task.
Total size of the datasets is over 18 milllion characters for MLPA-400 and almost double that for MLPA-400AV.

URL to repo: [https://github.com/dainis-boumber/MLP-400-datasets]

[MLPA-400](https://github.com/dainis-boumber/AA_CNN/wiki/MLPA-400-Dataset)
======

we considered a realistic problem of multilabel AA in the realm of scientific publications by creating a publicly available dataset consisting of 400 Ma-
chine Learning papers, Machine Learning Papers’ Authorship 400 (MLPA-400). To the best of our knowledge, multi-label AA of scientific publications has not received
a lot of attention. It deserves more attention because automatic resolution of authorship issues in papers can have a variety of downstream applications in intellectual property 
managements, citation analysis, archival systems, and author disambiguation. The task is challenging: papers have many authors whose writing style can evolve or influenced 
by colleagues, they contain direct quotes from other works, authors’ contribution to the paper in terms of the amount of text written is unknown; the number of papers and authors is large.

Considerations
======

Many approaches to creating a suitable corpus exist. For example, papers can be chosen across domains. However, even within one domain the stylistic differences between
venues are significant enough to make individual style hard to detect. A random sample of authors can be taken, but the number of multi-labeled documents would be few. Another possibility 
is taking the transitive closure of the set of co-authors and extracting at least k papers per author. However, creation of such a dataset for any reasonable k results in a very large transitive set.

Design
======

Using Google Scholar as a source, we created a list of top 20 authors in Machine Learning, ranked by the number of citations. We ensured a reasonable number of papers had an overlap of authors 
(i.e., we also included pa-pers that were jointly authored by the set of authors). For each author, 20 papers were downloaded for a total of 400
publications for the entire dataset. Each work is assigned 20 binary labels. The labels indicate which of the authors contributed to the paper’s creation. 100 papers out of 400 have more than one author from the 20 listed.
The number of authors ranged from 1 to 3 and the average was 1.2925. The text was extracted from the PDF files using pdfminer (Hinyama, 2017) and pre-processed. The title, authorship information, and bibliography fields were removed from each paper to ensure the classifier abides by
the rules of blind review instead of simply using author list while learning authorship. Formulas, table and figure captions were retained as they may contain valuable author specific style and topic information. 
The dataset is available here:

URL to repo: [https://github.com/dainis-boumber/AA_CNN/wiki/MLPA-400-Dataset]

If you find this dataset useful, please cite as follows: 

Dainis Boumber, Yifan Zhang and A. Mukherjee. "Experiments with convolutional neural networks for multi-label authorship attribution." Proceedings of the Eleventh International Conference on Language Resources and Evaluation (LREC 2018), Paris, France, 2018. European Language Resources Association (ELRA).

[MLP-400AV](https://github.com/dainis-boumber/MLP-400-datasets/tree/master/MLP-400AV)
======

Machine Learning Papers 400 Authorship Verification (MPL-400AV) dataset contains 20 publications by each of the top-20 authors in ML, for the total of 400.
The data is located in av-feature-generator project's ./ml_dataset directory. You can also obtain it as a tarball from

Format: csv

Author, Known_paper, Unknown_paper, Is_same_author

The data is split under to schemas: A and B. For both schemas, unknown samples is not present amongst the known ones, unlike in PAN (this can be changed easily)

Schema A: disjoint sets (Train, Val and Test do NOT intersect), disjoint subsets (papers appear only once, thus authors DO NOT intersect)

A balanced dataset, which is formed as follows:

Papers for each author are shuffled
Authors are shuffled
From each, we sample 70% for training, 10% for validation and 20% for testing, forming 3 subsets
Then by only using data from within each of the subsets from (2), we designate papers whose author is "unknown", without replacement
Therefore, while there is some intersection between the authors, none of the papers are present in more than one of subsets formed.

The results are saved in Atest.csv, Aval.csv and Atrain.csv

Schema A2: disjoint sets (Train, Val and Test do NOT intersect), but papers can appear more than once, thus authors DO intersect. For ex., negative samples are considered to be part of the "world" and can also be used more than once.

A balanced dataset, which is formed as follows:

Papers for each author are shuffled
Authors are shuffled
From each, we sample 70% for training, 10% for validation and 20% for testing, forming 3 subsets
Then by only using data from within each of the subsets from (2), we designate papers whose author is "unknown", with replacement
The results are saved in A2test.csv, A2val.csv and A2train.csv

Schema B: Train, Val and Test do MAY intersect

A balanced dataset, which is formed as follows:

Papers for each author are shuffled
Authors are shuffled
For each author, we designate papers whose author is "unknown"
From each, we sample 70% for training, 10% for validation and 20% for testing, forming 3 subsets
Then by only using data from within each of the subsets from (2), we designate papers whose author is "unknown"
Some of the papers present in one subset can be in the other, as well. For example a paper from Test can serve as a negative example in Train.

The results are saved in Btest.csv, Bval.csv and Btrain.csv

test.csv test , 20% of the data val.csv - validation, 10% of the data train.csv - traininig set, 70% of the data.

The dataset is produced using MLPA-400's Labels.csv which contains the ground truths for the paper authorship in the following format: ,<author_1>,...<author_20>\n is plain text and <author_n> is a digit 0 or 1 indicating whether this author is one of the co-authors. The first row is the header row.

See [MLPA-400](https://github.com/dainis-boumber/AA_CNN/wiki/MLPA-400-Dataset) for more details.

URL to repo: [https://github.com/dainis-boumber/MLP-400-datasets/tree/master/MLP-400AV]
