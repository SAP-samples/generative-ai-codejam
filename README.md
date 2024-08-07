# Containing Files

1. The LICENSE file:
In most cases, the license for SAP sample projects is `Apache 2.0`.

2. The .reuse/dep5 file: 
The [Reuse Tool](https://reuse.software/) must be used for your samples project. You can find the .reuse/dep5 in the project initial. Please replace the parts inside the single angle quotation marks < > by the specific information for your repository.

# CodeJam - Getting started with Generative AI Hub on SAP AI Core

<!--- Register repository https://api.reuse.software/register, then add REUSE badge:
[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/REPO-NAME)](https://api.reuse.software/info/github.com/SAP-samples/REPO-NAME)
-->

## Description
This repository contains the material for the "Getting strted with the Generative AI Hub on SAP AI Core" CodeJam, brought to you by the Developer Advocates at SAP.

## Overview
In this CodeJam you will learn how to use Generative AI Hub on SAP AI Core to implement a retrieval augmented generation (RAG) use case to improve the responses of large language models (LLMs) and reduce hallucinations. You will learn how to deploy an LLM on SAP AI Core and query it via SAP AI Launchpad and the Python SDK. Furthermore, you will learn about the most important genAI concepts and create and use text chunks and embeddings to improve your RAG response.

## Requirements

The requirements necessary to complete the exercises in this repository, including hardware and software specifications, are outlined in the [prerequisites](prerequisites.md) file.

### Exercises

You can find all exercises in the exercises folder. We will work through the exercises in the order shown here. From a session flow perspective, we are taking the "coordinated" approach:

The instructor will start you on the first exercise, and that's the only one you should do. You should only proceed to the next exercise once the instructor tells you to.

00. [Connect SAP AI Core and SAP AI Launchpad](exercises/00-connect-AICore-and-AILaunchpad.md)
01. [Deploy a Large Language Model (LLM) on SAP AI Core](exercises/01-deploy-model.md)
02. [Explore the Prompt Editor in SAP AI Launchpad](exercises/02-explore-genai-hub.md)
03. [Setup your Python environment](exercises/03-setup-python-environment.md)
04. [Create embeddings for your document chunks](exercises/04-create-embeddings.ipynb)
05. [Prompt an LLM](exercises/05-prompt-llm.ipynb)
06. [Store embeddings](exercises/06-store-embeddings-hana.ipynb)
07. [Implement the RAG use case](exercises/07-RAG.ipynb)

## Feedback

If you can spare a couple of minutes at the end of the session, please provide feedback to help us improve next time.

Use this [Give feedback](https://github.com/SAP-samples/generative-ai-codejam/issues/new?assignees=&labels=feedback&template=session-feedback-template.md&title=Session%20Feedback) link to create a special "feedback" issue, and follow the instructions in there.

Thank you!

## Other CodeJams

### CodeJam repositories

* [Service integration with SAP Cloud Application Programming Model](https://github.com/SAP-samples/cap-service-integration-codejam)
* [CodeJam - Getting Started with Machine Learning using SAP HANA and Python](https://github.com/SAP-samples/hana-ml-py-codejam)
* [Hands-on with the btp CLI and APIs](https://github.com/SAP-samples/cloud-btp-cli-api-codejam)
* [CodeJam - Combine SAP Cloud Application Programming Model with SAP HANA Cloud to Create Full-Stack Applications](https://github.com/SAP-samples/cap-hana-exercises-codejam)
* [All CodeJams in one list](https://github.com/orgs/SAP-samples/repositories?language=&q=Codejam&sort=&type=all)

### CodeJam Community

* [SAP CodeJam Events](https://community.sap.com/t5/sap-codejam/eb-p/codejam-events)
* [SAP CodeJam Community](https://community.sap.com/t5/sap-codejam/gh-p/code-jam)
* [SAP CodeJam Discussions](https://community.sap.com/t5/sap-codejam-discussions/bd-p/code-jamforum-board)

## Acknowledgements

The exercise content in this repository is based on different sample repositories created by the SAP AI Core team. 

The exercises related to the prerequisites and setting up BAS were copied and adjusted from my colleague [Vitaliy's](https://www.linkedin.com/in/witalij/?originalSubdomain=pl) **CodeJam - Getting Started with Machine Learning using SAP HANA and Python**.


## How to obtain support
[Create an issue](https://github.com/SAP-samples/<repository-name>/issues) in this repository if you find a bug or have questions about the content.
 
For additional support, [ask a question in SAP Community](https://answers.sap.com/questions/ask.html).

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSE) file.
