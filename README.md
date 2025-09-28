# UTR-CODE
#  RiboDecode: Deep Generative Optimization of mRNA Codon Sequences for Enhanced mRNA Translation and Therapeutic Efficacy.

## Overview
RiboDecode is a deep learning-based tool designed to optimize mRNA codon sequences to enhance mRNA translation and therapeutic efficacy. This repository provides the necessary code and resources to predict and optimize mRNA translation levels in various cellular environments.

## Environment
To set up the environment, ensure you have the following dependencies installed:

- Python=3.8.19
- torch=2.0.1
- CUDA=12.1  
- viennarna=2.6.4 
- numpy=1.24.4  
- pandas=2.0.3
- p-tqdm=1.4.0 
- matplotlib=3.7.5 
- seaborn=0.13.2

The required dependency packages will be automatically downloaded the first time you run the program.

## **Installation and Usage**

You can create a new conda environment using the following command:

```
conda create -n ribodecode python=3.8
```

Activate the environment:

```
conda activate ribodecode
```

### **TranslationModel**

Download the necessary **.whl** file from [here](https://drive.google.com/file/d/19Yyl8uUbjQn0TAA4E52ZUGBd_pb_RyW8/view?usp=sharing) and install it using:

```
pip install TranslationModel-1.1.0-py3-none-any.whl
```

To perform local testing, use the following command:

```
pred-translation --cds ATGGACGGGTAG --env HEK293T
```

* The maximum length of the coding sequence (**cds**) should not exceed 4500nt.

* Pre-configured cellular environments (**env**): **HEK293T**, **A549**, and **HeLa**. 

For custom cellular environments, use:

```
pred-translation --cds ATGGACGGGTAG --csv env_file.csv
```

Here, '**csv**' specifies the custom cellular environment file. We provide a standard template file, **env_file.csv**, with the following format:
The first column contains human gene IDs, which must remain unchanged.
The second column lists the corresponding mRNA RPKM values, provided by the user. Missing values can be replaced with 0.

If you have any questions about the TranslationModel, you can get help information by using the following command:

```
pred-translation --help
```
