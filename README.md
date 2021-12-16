# Hugo_research
## Introduction
This repository contains the methodology and code for my research project made under supervision of Hugo Schyns.
## Content
### Data cleaning
* What to do when companies change their TIC code, use CUSIP?
Read up on the litterature about this subject. Hugo told me that many financial analysts/auditors use CUSIP.
* Missing values:
Approach mentioned in the paper and also supported by Hugo:
    1. If possible, fill forward.
    2. If not possible, compute median from cross-section.
* How do you handle string values, one-hot encoding?
There are no string values.
### Data structuring
* Training, validition and test sample: do this in a rolling window, but which kind is best (there are three main methods)?  
Hugo suggested to first structure your time series into multiple windows (e.g. 12/3,23/4, etc.) and then use one of the two possibilities:
    1. Randomly select windows for training set and test set. This generalises better, but kind of look like data leakage to me.
    2. Select first x% for training and last (100-x)% for test.
    