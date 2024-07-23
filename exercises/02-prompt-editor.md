## [1/2] Use the Chat in Generative AI Hub
Open the Generative AI Hub tab and select Chat. Now click Configure and have a look at the available fields. The selected model will show your model once it is deployed. If there is no deployment this will be empty and you will not be able to chat. If you have more than one large language model deployed you will be able to select which one you want to use here. 

The parameter frequency penalty allows you to penalize words that appear too frequently in the text, leading to the model not sounding too robotic. Similarly the higher the presence penalty, the more likely the model will talk about new topics, as you penalize words that have appeared in the text so far. With Max Tokens you can set the size of the input and output of the model. Where tokens are not words but rather 4-5 characters long. With the Temperature parameter you can set how creative the model should sound so flexible the model is allowed to be in selecting the next token in the sequence.

![Chat](images/2024-07-22_15-32-44.png)

In the Chat Context tab right under Context History you can set the number of messages that should be send to the model. So how much of the chat history should be provided as context to the model for each new request. You can add a System Message to describe the role or give more information of what is expected from the model. You can also provide example inputs and outputs.

![Chat](images/2024-07-22_15-40-33.png)

## [2/2] Use the Prompt Editor in Generative AI Hub

