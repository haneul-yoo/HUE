# HUE: Hanja Understanding Evaluation

The repository contains the HUE dataset and Hanja language models, and the code baselines to implement them.
See our paper for more details about HUE and Hanja PLMs.

## HUE dataset

### Benchmark Datasets

HUE is composed of 4 tasks:
* Chronological Attribution (CA)
* Topic Classification (TC)
* Named Entity Recognition (NER)
* Summary Retrieval (SR)

HUE aims to encourage training Hanja language models that help to analyze the Korean historical documents written in Hanja which is an extinct language.

### Dataset Size

You can download all 12 [here](https://drive.google.com/drive/folders/1e0i9yM9PSifCOMFr3HXmvAOxcXjcNlI7?usp=sharing), or individually from the table below:

|     |         Train       |       Dev         |       Test        |
|:---:|:-------------------:|:-----------------:|:-----------------:|
|  [CA](https://drive.google.com/drive/folders/1f9YSpdMEYvOM5nAt4GdK_1XMV_MWt9JO?usp=sharing) | [330,469 (672.1 MB)](https://drive.google.com/file/d/1B-3o_TG1bGLpCPDc4sqFD2SugZ6aCI5t/view?usp=sharing)  | [41,309 (84.2 MB)](https://drive.google.com/file/d/1dGn7ETF7211-JlHjA3LKp07vBegFuETw/view?usp=sharing)  | [41,309 (83.3 MB)](https://drive.google.com/file/d/1ZjnZiBhOBqQfd-GDkzacAUhFK3QOdwUv/view?usp=sharing)  |
|  [TC](https://drive.google.com/drive/folders/1Tmi76k9pkjzUIKi6FquLDjEMi0TYMbHP?usp=sharing) | [330,424 (188.6 MB)](https://drive.google.com/file/d/1Jdw_QEUe68GYx3xCGOvfA0CNlUXnEmM6/view?usp=sharing)  | [41,303 (23.8 MB)](https://drive.google.com/file/d/1ZW_0GjpblW1P_6Q44i25wZ0QBxIE66Kd/view?usp=sharing)  | [41,304 (23.4 MB)](https://drive.google.com/file/d/1Jdw_QEUe68GYx3xCGOvfA0CNlUXnEmM6/view?usp=sharing)  |
| [NER](https://drive.google.com/file/d/11uEye8ZuFJDVZhMW6QtasykiDU_PX-qN/view?usp=sharing) | [385,915 (480.9 MB)](https://drive.google.com/file/d/1NUNqOXxZsYm-bf-7lKv390MOs_b2oVqf/view?usp=sharing)  | [13,417 (8.4 MB)](https://drive.google.com/file/d/18rajyvjXjGcHXq5irmqQ6yAdb3JVwEBC/view?usp=sharing)   | [13,418 (8.4 MB)](https://drive.google.com/file/d/1VHwHVOnKDTkxweBSngpn0Gm_WfaJGqBR/view?usp=sharing)   |
|  [SR](https://drive.google.com/drive/folders/1NSqf3wOaFYiJVZYKLDB-uf3-xu2CR6Cv?usp=sharing) | [169,840 (1.22 GB)](https://drive.google.com/file/d/11uEye8ZuFJDVZhMW6QtasykiDU_PX-qN/view?usp=sharing)   | [21,570 (155.8 MB)](https://drive.google.com/file/d/18rajyvjXjGcHXq5irmqQ6yAdb3JVwEBC/view?usp=sharing) | [21,296 (153.9 MB)](https://drive.google.com/file/d/1VHwHVOnKDTkxweBSngpn0Gm_WfaJGqBR/view?usp=sharing) |


## Hanja language models

### Model Download

| Model Name          |   Size   |
|---------------------|----------|
| [AnchiBERT + AJD/DRS](https://drive.google.com/drive/folders/1VDZy9LrlaQKrPCeFqWnnZzBdholSDem2?usp=sharing) | 379.2 MB |
| [mBERT + AJD/DRS](https://drive.google.com/drive/folders/1trPpBglD8rM8FeeQaXpfWOXh6vxYRNwt?usp=sharing)     | 379.2 MB |

## Code Baselines

Make sure you have installed the packages listed in environment.yml.
If you use conda, you can create an environment from this package with the following command:

```
conda env create -f environment.yml
```

Codes, data, and models should be placed in this directory tree.
```
HUE
├── code
│   ├── HUE_fine-tuning_Chronological_Attribution.ipynb
│   ├── HUE_fine-tuning_Named_Entity_Recognition.ipynb
│   ├── HUE_fine-tuning_Summary_Retrieval.ipynb
│   └── HUE_fine-tuning_Topic_Classification.ipynb
├── dataset
│   ├── HUE_Chronological_Attribution
│   │   ├── HUE_Chronological_Attribution.csv
│   │   ├── HUE_Chronological_Attribution_dev.csv
│   │   ├── HUE_Chronological_Attribution_test.csv
│   │   └── HUE_Chronological_Attribution_train.csv
│   ├── HUE_Named_Entity_Recognition
│   │   ├── HUE_Named_Entity_Recognition_dev.csv
│   │   ├── HUE_Named_Entity_Recognition_test.csv
│   │   └── HUE_Named_Entity_Recognition_train.csv
│   ├── HUE_Summary_Retrieval
│   │   ├── HUE_Summary_Retrieval_dev.csv
│   │   ├── HUE_Summary_Retrieval_test.csv
│   │   └── HUE_Summary_Retrieval_train.csv
│   └── HUE_Topic_Classification
│       ├── HUE_Topic_Classification.csv
│       ├── HUE_Topic_Classification_dev.csv
│       ├── HUE_Topic_Classification_test.csv
│       └── HUE_Topic_Classification_train.csv
├── model
│   ├── AnchiBERT+AJD-DRS
│   │   ├── config.json
│   │   ├── pytorch_model.bin
│   │   ├── special_tokens_map.json
│   │   ├── tokenizer_config.json
│   │   └── vocab.txt
│   └── mBERT+AJD-DRS
│       ├── config.json
│       ├── pytorch_model.bin
│       ├── special_tokens_map.json
│       ├── tokenizer_config.json
│       └── vocab.txt
└── tokenizer
    ├── AnchiBERT+AJD-DRS
    │   ├── special_tokens_map.json
    │   ├── tokenizer_config.json
    │   └── vocab.txt
    └── mBERT+AJD-DRS
        ├── special_tokens_map.json
        ├── tokenizer_config.json
        └── vocab.txt
```
