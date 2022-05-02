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

You can download all 12 [here](https://drive.google.com/drive/folders/1ogijSobaOvBw6vnVS1lnsAyTv4XM9rMK?usp=sharing), or individually from the table below:

|     |         Train       |       Dev         |       Test        |
|:---:|:-------------------:|:-----------------:|:-----------------:|
|  [CA](https://drive.google.com/drive/folders/1qfBJFNiMLgyFIoo4hznTFpkM5w9ctaU9?usp=sharing) | [330,469 (672.1 MB)](https://drive.google.com/file/d/1IzhaE3h_1CGzXJDBejY5GGeUnH1dEdLR/view?usp=sharing)  | [41,309 (84.2 MB)](https://drive.google.com/file/d/1L5xeIsp0H3iRgdh0nzLoqngSLH7p56AS/view?usp=sharing)  | [41,309 (83.3 MB)](https://drive.google.com/file/d/1rwoEzXnsEQP-O33QZcZtApwvifU6rM35/view?usp=sharing)  |
|  [TC](https://drive.google.com/drive/folders/1sGfm_07jf5QSRz0ldpIOqKnMeyp5QH0w?usp=sharing) | [330,424 (188.6 MB)](https://drive.google.com/file/d/1wsG9dNYC6VdBOy6GJuJBGL4NiQvQNl39/view?usp=sharing)  | [41,303 (23.8 MB)](https://drive.google.com/file/d/1aFik0DKvHCu1S1SK6rcHHW4ws2Az5iYy/view?usp=sharing)  | [41,304 (23.4 MB)](https://drive.google.com/file/d/1nauljoWrMRwU7EmErM9JepIh3iLZRyg8/view?usp=sharing)  |
| [NER](https://drive.google.com/drive/folders/18cBdy251yIvFF9dIt78hq7d9W-AjCg4E?usp=sharing) | [385,915 (480.9 MB)](https://drive.google.com/file/d/1NUNqOXxZsYm-bf-7lKv390MOs_b2oVqf/view?usp=sharing)  | [13,417 (8.4 MB)](https://drive.google.com/file/d/17GgItjhhVMjpGkmcno4nL3bfclP16viL/view?usp=sharing)   | [13,418 (8.4 MB)](https://drive.google.com/file/d/1ytg8GXK1b7-rAtusVfxkKv8JmZX6FuQl/view?usp=sharing)   |
|  [SR](https://drive.google.com/drive/folders/1fgiKlH2QKMtqBW1vbvIkaiS-irvmzC4D?usp=sharing) | [169,840 (1.22 GB)](https://drive.google.com/file/d/1wUcKGfQumJRRR4sIaCB_Z_p4al8WwJQz/view?usp=sharing)   | [21,570 (155.8 MB)](https://drive.google.com/file/d/1p8jOBiIJAOi2l8zem2BXFEBqnSPMl1nY/view?usp=sharing) | [21,296 (153.9 MB)](https://drive.google.com/file/d/1w0vcSvkVRfyD8Z3W7S29EJvhAJ3lji8p/view?usp=sharing) |


## Hanja language models

### Model Download

| Model Name          |   Size   |
|---------------------|----------|
| [AnchiBERT + AJD/DRS](https://drive.google.com/drive/folders/1qSHEU5GYrFRoHPsKKubEaVmQ3VaPUoTX?usp=sharing) | 379.2 MB |
| [mBERT + AJD/DRS](https://drive.google.com/drive/folders/1lJUr8ZCM6utPUYKFBiEWPEuDOSWUq-t9?usp=sharing)     | 379.2 MB |

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
