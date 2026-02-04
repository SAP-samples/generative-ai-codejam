# Orchestration Service in SAP AI Launchpad
The orchestration service of Generative AI Hub lets you use all the available models with the same codebase. You only deploy the orchestration service and then you can access all available models simply by changing the model name parameter. You can also use grounding, prompt templating, data masking and content filtering capabilities.

This YouTube video ([AI Foundation: Orchestration workflow with grounding using S3](https://youtu.be/f2hgGgpLIn0)) shows the steps of the following exercise.


👉 Open **[SAP AI Launchpad](https://genai-codejam-luyq1wkg.ai-launchpad.prod.eu-central-1.aws.ai-prod.cloud.sap/aic/index.html#/workspaces&/a/detail/TwoColumnsMidExpanded/?workspace=ai-codejam&resourceGroup=s3-grounding)**

## [1/3] Select `s3-grounding` Resource Group
👉 Go to **Workspaces** and select the `s3-grounding` resource group.

![s3 resource group](images/s3-grounding-resource-group.png)

## [2/3] Create Grounding Pipeline

👉 Go to **SAP AI Core Administration > Generic Secrets** and check whether an S3 bucket is added. DO NOT DELETE IT!

![generic secret](images/generic-secret.png)

👉 Go to **Generative AI Hub > Grounding Management**.

![grounding management 1](images/grounding-management-1.png)

👉 Select the available pipeline and have a look at the documents, chunks and metadata.

![grounding management 2](images/grounding-management-2.png)

👉 Select the three dots in the top right corner and click **Run Search**.

👉 Type the question you want to ask to see which chunk would be retrieved. This is not a RAG pipeline yet, so there is no model to answer your question. This is simply to check which chunks would be retrieved for your use case.

👉 Select your pipeline and run the search.

![grounding management 3](images/grounding-management-3.png)

## [3/3] Build an Orchestration Workflow with your Grounding Pipeline

👉 Expand Generative AI Hub and select Orchestration from the menu list to see the Orchestration Workflow.

👉 The Orchestration Configurations page will open, where any existing orchestration workflow configurations are displayed.

👉 Select the **Create** button to create a new configuration.

![orchestration create](images/Orchestration-Create.png)

👉 The Orchestration Configuration page will open where you can configure multiple settings for a range of different modules such as **Grounding, Data Masking, Filtering and Tanslation**.

![orchestration configuration](images/Orchestration-TurnOn_AdvancedModules.png)

👉 Toggle the **Advanced setting** to ON to see the different modules available. You will notice that some of these are mandatory, while others are optional:

👉 The **Input** variable will hold your user input, question or query.

👉 The **Output** variable will hold the text chunk(s) that are retrieved from your grounding pipeline.

👉 Enable the **Grounding Management** option

![orchestration Grounding Enable](images/Orchestration-TurnOn_AdvancedModules_DocumentGrounding.png)

👉 Set **Input**, **Output** variable and select the **pipeline**

![orchestration Grounding Enable](images/Orchestration-SetInput-Output-Pipeline.png)

👉 Make sure to either configure all of the other modules or turn them off. You can add **Input/Output Translation**, **Data Masking**, **Input/Output Filtering** by enabling the toggle option next to them.
 
👉 You can to select a **model** you want to use under **Model Configuration**.

![orchestration Select Model](images/Orchestration-SelectModel.png)

👉 Once all of the modules are configured or disabled you can **Run** the workflow.

![orchestration Ask Query](images/Orchestration-AskQuery.png)

👉 Add your question and run the orchestration workflow. You just build the same RAG (retrieval-augmented generation) use case as in exercise [06-RAG](06-RAG.ipynb).

![orchestration 6](images/orchestration-6.png)

👉 Give your configuration the name **Grounding_Configuration**, select **orchestration** as the Scenario Name and then select **Save**.

![orchestration Save config](images/Orchestration_GroundingConfig_Save.png)

> 👉 For the next exercises go to **Workspaces** and select your own resource groups again!

[Next Exercise](08-orchestration-service.ipynb)
