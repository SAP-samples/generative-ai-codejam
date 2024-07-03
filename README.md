# Containing Files

1. The LICENSE file:
In most cases, the license for SAP sample projects is `Apache 2.0`.

2. The .reuse/dep5 file: 
The [Reuse Tool](https://reuse.software/) must be used for your samples project. You can find the .reuse/dep5 in the project initial. Please replace the parts inside the single angle quotation marks < > by the specific information for your repository.

# CodeJam - Implement a Retrieval Augmented Generation (RAG) Use Case with generative AI hub on SAP AI Core, SAP AI Launchpad and Python.

<!--- Register repository https://api.reuse.software/register, then add REUSE badge:
[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/REPO-NAME)](https://api.reuse.software/info/github.com/SAP-samples/REPO-NAME)
-->

## Description
In this CodeJam you will learn how to use generative AI hub on SAP AI Core to implement a retrieval augmented generation (RAG) use case to improve the results of large language models (LLMs). You will learn how to deploy an LLM on SAP AI Core and query it via SAP AI Launchpad and the Python SDK. Furthermore, you will learn about the most important genAI concepts and create and use text chunks and embeddings to improve your RAG response.

## Requirements

The requirements necessary to complete the exercises in this repository, including hardware and software specifications, are outlined in the [prerequisites](prerequisites.md) file.

### Exercises

During the CodeJam we will go through each exercise one by one. If you complete any exercise ahead of others, kindly refrain from moving on to the next one. Instead, take the opportunity to delve deeper into what you've just learned and check out the questions at the end of each exercise.

Here's an overview of the exercises in this CodeJam.

> Make certain that you have successfully completed all the [prerequisites](prerequisites.md)

Setup:

* [Setup SAP Business Application Studio and a dev space](exercises/00-setup/setup-bas.md)

Machine Learning:

1. [Check your setup](exercises/010-check_setup.ipynb)
1. [(Optional) Basics of HANA DataFrames](exercises/020-dataframes.ipynb)
1. [Exploratory Data Analysis, or EDA](exercises/030-UnifiedReportDF-EDA.ipynb)
1. [Training a ML model using Classification](exercises/040-Classification-RDT-FirstFit.ipynb)
1. [Training a ML model using Train/Test split](exercises/041-Classification-RDT-TrainTestSplit-Implicit.ipynb)
1. [Preprocessing - Exclude High Cardinality](exercises/050-RDT-Preprocessing-ExcludeHighCardinality.ipynb)
1. [Preprocessing - Missing Values](exercises/051-RDT-Preprocessing-MissingValues.ipynb)
1. [Preprocessing - Feature Engineering](exercises/052-RDT-Preprocessing-FE.ipynb)
1. [Model tuning](exercises/060-RDT-Tuning-Hyperparameters.ipynb)
1. [Auto ML](exercises/070-RDT-AutoML.ipynb)


## Download and Installation

## Known Issues
<!-- You may simply state "No known issues. -->

## How to obtain support
[Create an issue](https://github.com/SAP-samples/<repository-name>/issues) in this repository if you find a bug or have questions about the content.
 
For additional support, [ask a question in SAP Community](https://answers.sap.com/questions/ask.html).

## Contributing
If you wish to contribute code, offer fixes or improvements, please send a pull request. Due to legal reasons, contributors will be asked to accept a DCO when they create the first pull request to this project. This happens in an automated fashion during the submission process. SAP uses [the standard DCO text of the Linux Foundation](https://developercertificate.org/).

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSE) file.
