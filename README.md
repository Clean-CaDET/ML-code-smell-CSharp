# ML-code-smell-CSharp
This repository contains the reproducibility package for the paper "Automatic detection of code smells using metrics and CodeT5 embeddings: a case study in C#".

# Dataset

A dataset containing code snippets from C# projects, annotated for the presence of Long Method and Large Class code smells:
* [Long Method](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Dataset/DataSet_Long%20Method%20-%20Round%203.xlsx)
* [Large Class](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Dataset/DataSet_Large%20Class%20-%20Round%203.xlsx).

We prepare our experiment by dividing the dataset into the training (80%) and test (20%) datasets via a stratified random sampling strategy (Jupyter notebooks https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Dataset/Large_Class_prepare_dataset.ipynb and https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Dataset/Long_Method_prepare_dataset.ipynb) and save the train and test portions to the pickle files.

A detailed description of the dataset, its collection, and annotation procedure is presented in the paper 
Luburić, N., Prokić, S., Grujić, K.G., Slivka, J., Kovačević, A., Sladić, G. and Vidaković, D., 2021. Towards a systematic approach to manual annotation of code smells.
https://www.techrxiv.org/articles/preprint/Towards_a_systematic_approach_to_manual_annotation_of_code_smells/14159183/1

# Heuristics

Jupyter notebooks evaluating the performance of metric-based code smell detection heuristics on our dataset:
* [Large Class](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Heuristics/Large_Class_Heuristics.ipynb)
* [Long Method](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Heuristics/Long_Method_Heuristics.ipynb)

# Metrics

Jupyter notebooks evaluating the performance of the ML classifier trained using source code metrics as features:
* [Large Class](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Metrics/Large_Class.ipynb)
* [Long Method](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/Metrics/Long_Method.ipynb)

# CodeT5

Jupyter notebooks evaluating the performance of the ML classifier trained using CodeT5 neural source code embeddings as features:
* [Large Class](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/CodeT5/Large_Class.ipynb)
* [Long Method](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/CodeT5/Long_Method.ipynb).

The embedding representation is available as Python pickle DataFrames:
* [Large Class](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/CodeT5/CodeT5_embeddings_LC.pkl)
* [Long Method](https://github.com/Clean-CaDET/ML-code-smell-CSharp/blob/master/CodeT5/CodeT5_embeddings_LM.pkl).

# Error analysis

In [https://github.com/Clean-CaDET/ML-code-smell-CSharp/tree/master/Dataset/Error%20analysis] we provide the details of analyzing the errors our best model (the ML classifier trained using source code metrics as features) makes on the test set.
