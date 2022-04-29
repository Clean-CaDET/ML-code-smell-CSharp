# ML-code-smell-CSharp
This repository contains the reproducibility package for the paper "Automatic detection of code smells using metrics and CodeT5 embeddings: a case study in C#".

# Dataset

A dataset containing code snippets from C# projects, annotated for the presence of Long Method and Large Class code smells:
* [Long Method](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Dataset/DataSet_Long%20Method%20-%20Round%203.xlsx)
* [Large Class](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Dataset/DataSet_Large%20Class%20-%20Round%203.xlsx).

We prepare our experiment by dividing the dataset into the training (80%) and test (20%) datasets via a stratified random sampling strategy (Jupyter notebooks https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Dataset/Large_Class_prepare_dataset.ipynb and https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Dataset/Long_Method_prepare_dataset.ipynb) and save the train and test potrions to the picke files.

A detailed description of the dataset, its collection, and annotation procedure is presented in the paper 
Luburić, N., Prokić, S., Grujić, K.G., Slivka, J., Kovačević, A., Sladić, G. and Vidaković, D., 2021. Towards a systematic approach to manual annotation of code smells.
https://www.techrxiv.org/articles/preprint/Towards_a_systematic_approach_to_manual_annotation_of_code_smells/14159183/1

# Heuristics

Jupyter notebooks evaluating the performance of metric-based code smell detection heuristics on our dataset.

# Metrics

Jupyter notebooks evaluating the performance of the ML classifier trained using code metrics as features.

# CodeT5

Jupyter notebooks evaluating the performance of the ML classifier trained using CodeT5 neural source code embeddings as features. The embedding representation is avalilable as Python pickle dataframes.
