# Fabric AI Assistant
This repo explores ways to integrate Microsoft Fabric AI Skills into Azure AI Agent Service, enabling AI agents to query data through natural language. As it is currently not possible to call AI Skills from outside of Microsoft Fabric, these experiments are confined to Python notebooks running within Fabric.

Note that this version was last updated for version 1.0.0b5 of azure-ai-projects.

To try out the assistant, perform the following steps:
1. Follow the [setup instructions of the Azure AI Agent Service quickstart](https://learn.microsoft.com/en-us/azure/ai-services/agents/quickstart?pivots=programming-language-python-azure).
1. [Create an app registration](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app?tabs=certificate) and give it permissions to the newly created AI resources.
1. In Microsoft Fabric, [Create an AI Skill](https://learn.microsoft.com/en-us/fabric/data-science/how-to-create-ai-skill) and publish it.
1. [Import the notebook into your Fabric workspace](https://learn.microsoft.com/en-us/fabric/data-engineering/how-to-use-notebook#import-existing-notebooks).
1. Add values to the notebook's parameter cell, incl. Azure AI authentication details and URL of your published AI Skill.
1. Modify the doc string of the ```ask_about_data``` function to correspond to the data of your AI Skill.
1. Modify the cell containing the user input to include your query.
1. Run the entire notebook.