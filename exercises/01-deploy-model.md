# Deploy a proxy for an LLM on SAP AI Core
With Generative AI Hub on SAP AI Core you have access to all major large language models (LLMs). There are open-source models that SAP has deployed such as the **Falcon** model. And there are models that SAP is a proxy for, such as the GPT models, Google models, models provided by Amazon Bedrock and more. To use one of the provided LLMs for a custom use case you need to create a deployment configuration of the model. Using the configuration you can then deploy the model. You will then get a deployment url that is created for you to query the model of your choice.

## Create a configuration to deploy a proxy for a large language model on SAP AI Core
With Generative AI Hub on SAP AI Core you have access to all major large language models (LLMs). There are open-source models that SAP has deployed such as the **Falcon** model. And there are models that SAP is a proxy for, such as the GPT models, Google models, models provided by Amazon Bedrock and more. To use one of the provided LLMs for a custom use case you need to create a deployment configuration of the model. Using the configuration you can then deploy the model. You will then get a deployment url that is created for you to query the model of your choice.

👉 Open the ML Operations tab, go to Scenarios and select the foundation-models scenario. This is the only pre-configured scenario from SAP. For all other custom machine learning models you would want to train or deploy you need to create your own scenario.

![Scenarios 1/2](images/2024-07-22_12-52-11.png)

👉 Select the Executables tab and then the serving executable azure-openai to see the available Azure OpenAI models.

![Scenarios 2/2](images/2024-07-22_13-04-27.png)

👉 Copy the name of the model you want to deploy the proxy for. In this CodeJam we will use gpt-35-turbo.
After that we will create a configuration.

![Available models](images/2024-07-22_13-04-40.png)

👉 Create a new configuration.

![Configurations](images/2024-07-22_13-15-51.png)

👉 Enter a configuration name of your choice, select the foundation-models scenario, version and the executable **azure-openai**. Click next.

![Create configuration 1/4](images/2024-07-16_16-42-19.png)

👉 Paste the model name gpt-35-turbo into the modelName field and click next.

```
gpt-35-turbo
```

![Create configuration 2/4](images/2024-07-16_16-42-54.png)

👉 Click Review on the bottom of the page.

![Create configuration 3/4](images/2024-07-16_16-43-20.png)

👉 Review the configuration and click create.

![Create configuration 4/4](images/2024-07-16_16-43-35.png)

## Deploy a proxy for a large language model on SAP AI Core

👉 Click on Create Deployment to create a deployment for that configuration. This will not actually deploy the model but it will deploy a proxy that will return a URL for you to use to query the large language model you specified in the configuration.

![Create deployment 1/5](images/2024-07-16_16-43-57.png)

👉 For the duration select **Standard**. You can also select **Custom** to have the deployment available for a limited time. Click Review.

![Create deployment 2/5](images/2024-07-16_16-44-17.png)

👉 Click Create.

![Create deployment 3/5](images/2024-07-16_16-44-32.png)

Once the deployment is running you will receive a URL to query the model. Wait a couple of minutes, then refresh the page for the URL to appear.

![Create deployment 4/5](images/2024-07-16_16-44-49.png)

Using the URL, the client id and the client secret from the SAP AI Core service key, you could now already query the model using any programming language or any API platform.

☝️ You will need the deployment ID of this models and of the embedding model you will deploy in the next step in [Exercise 09-create-connection-configuration](../09-create-connection-configuration/README.md).

![Create deployment 5/5](images/2024-07-16_16-51-40.png)

## Deploy a proxy for an embedding model on SAP AI Core
👉 To implement a retrieval augmented generation (RAG) use case we also need to deploy an embedding model. The embeddings for our text chunks will then be stored in a vector database (e.g. HANA Vector Store). To deploy the embedding model repeat the steps above using the model name **text-embedding-ada-002** instead of **gpt-4**: 
```
text-embedding-ada-002
```
## Summary

At this point, you will have learned which models are available via Generative AI Hub and how to deploy LLMs in SAP AI Launchpad.

## Further reading

* [SAP AI Launchpad - Help Portal (Documentation)](https://help.sap.com/docs/ai-launchpad/sap-ai-launchpad/what-is-sap-ai-launchpad)
* [SAP AI Core Terminology](https://help.sap.com/docs/sap-ai-core/sap-ai-core-service-guide/terminology)
* [Available Models in the Generative AI Hub](https://help.sap.com/docs/sap-ai-core/sap-ai-core-service-guide/models-and-scenarios-in-generative-ai-hub)

---

[Next exercise](02-prompt-editor.md)
