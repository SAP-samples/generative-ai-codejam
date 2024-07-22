## [1/3] Create a Configuration to Deploy a Proxy for a Large language Model on SAP AI Core

Open the ML Operations tab, go to Scenarios and select the foundation-models scenario. This is the only pre-configered scenario from SAP. For all other custom machine learning models you would need to create your own scenario.

![Scenarios](images/2024-07-22_12-52-11.png)

Select the Executables tab and then the serving executable azure-openai to see the available Azure OpenAI models.

![Scenarios](images/2024-07-22_13-04-27.png)

Copy the name of the model you want to deploy the proxy for. In this CodeJam we will use gpt-35-turbo.
After that we will create a configuration.

![Available models](images/2024-07-22_13-04-40.png)

Create a new configuration.

![Configurations](images/2024-07-22_13-15-51.png)

Enter a configuration name of your choice, select the foundation-models scenrario, version and the executable azure-openai. Click next.

![Create configuration 1](images/2024-07-16_16-42-19.png)

Paste the model name ```sh gpt-35-turbo``` into the modelName field and click next.

![Create configuration 2](images/2024-07-16_16-42-54.png)

Click Review on the bottom of the page.

![Create configuration 3](images/2024-07-16_16-43-20.png)

Review the configuration and click create.

![Create configuration 4](images/2024-07-16_16-43-35.png)

## [2/3] Deploy a Proxy for a Large language Model on SAP AI Core

Click on Create Deployment to create a deployment for that configuration. This will not actually deploy the model but it will deploy a proxy that will return a URL for you to use to query the large language model you specified in the configuration.

![Create deployment 1](images/2024-07-16_16-43-57.png)

For the duration select Standard. You can also select Custom to have the deployment available for a limited time. Click Review.

![Create deployment 2](images/2024-07-16_16-44-17.png)

Click Create.

![Create deployment 3](images/2024-07-16_16-44-32.png)

Once the deployment is running you will receive a URL to query the model. Refresh the page until the URL appears. This can take a couple of minutes.

![Create deployment 3](images/2024-07-16_16-44-49.png)

Using the URL and the client id and the client secret from the SAP AI Core service key, you could now already query the model using any programming language or any API platform.

![Create deployment 3](images/2024-07-16_16-51-40.png)

## [3/3] Deploy a Proxy for an Embedding Model on SAP AI Core
To implement a retrieval augmented generation (RAG) use case we also need to deploy an embedding model. The embeddings for our text chunks will then be stored in a vector database (e.g. HANA Vector Store). To deploy the embedding model repeat the steps above using the model name: ```sh text-embedding-ada-002```
