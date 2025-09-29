# UTR-CODE

## Overview
Translation is a fundamental biological process that directly influences protein abundance, yet the mechanisms by which mRNA sequences determine translational regulation remain incompletely understood, especially the 5’ untranslated regions (5' UTRs) play an essential role in translation regulation. Here, we generated 1,586 paired RNA-seq and Ribo-seq datasets from six species and developed a deep learning model UTR-CODE, to predict mRNA translation efficiency (TE). UTR-CODE demonstrates strong cross-species generalizability and outperforms existing tools across diverse platforms. 

## Environment
To set up the environment, ensure you have the following dependencies installed:

- Python=3.8.20
- torch=2.4.1
- CUDA=12.1  
- numpy=1.24.4
- pandas=2.0.3  
- scipy=1.10.1
- tqdm=4.67.1 
- pyarrow=17.0.0 

The required dependency packages will be automatically downloaded the first time you run the program.

## **Installation and Usage**

You can create a new conda environment using the following command:

```
conda create -n UTR-CODE python=3.8
```

Activate the environment:

```
conda activate UTR-CODE
```

### **UTR-CODE Model**

Download the necessary **.whl** file from [here](https://drive.google.com/file/d/19Yyl8uUbjQn0TAA4E52ZUGBd_pb_RyW8/view?usp=sharing) and install it using:

```
pip install utr_code-1.0.0-py3-none-any.whl
```

To perform local training, use the following command:

```
utr-code-train --epochs 10
```
Here, epochs represents the number of training rounds, the default value is 10.

After the training is completed, the training weights will be saved in the current directory.

## Version History

- **1.0 (2025-9-29)**

  Updata readme.md.
  
## Contact
For any questions, issues, or further assistance, please feel free to contact us via:
[@HeXin](https://github.com/TcbfGroup)

