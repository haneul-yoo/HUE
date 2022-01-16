# HUE: Hanja Understanding Evaluation

The repository contains the HUE dataset and Hanja language models, and the code baselines to implement them.
See our paper for more details about HUE and Hanja PLMs.

## HUE dataset

### Benchmark Datasets

HUE is composed of 4 tasks:
* King Prediction (KP)
* Topic Classification (TC)
* Named Entity Recognition (NER)
* Summary Retrieval (SR)

HUE aims to encourage training Hanja language models that help to analyze the Korean historical documents written in Hanja which is an extinct language.

### Dataset Size

You can download all 12 from here, or individually from the table below:

|     |    Train   |    Dev    |    Test   |
|:---:|:----------:|:---------:|:---------:|
|  KP | 330,469 () | 41,309 () | 41,309 () |
|  TC | 330,424 () | 41,303 () | 41,304 () |
| NER | 385,915 () | 13,417 () | 13,418 () |
|  SR | 169,840 () | 21,570 () | 21,296 () |


## Hanja language models

### Model Download

| Model Name          | Size | Link |
|---------------------|------|------|
| AnchiBERT + AJD/DRS |      |      |
| mBERT + AJD/DRS     |      |      |

## Code Baselines

Make sure you have installed the packages listed in environment.yml.
If you use conda, you can create an environment from this package with the following command:

```
conda env create -f environment.yml
```

Codes, data, and models should be placed in this directory tree.
```

```
