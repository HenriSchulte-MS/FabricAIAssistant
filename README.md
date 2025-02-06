# Fabric AI Assistant
This repo explores ways to integrate Microsoft Fabric AI Skills and Semantic Link into AI agents, enabling these agents to query data through natural language. As it is currently not possible to call AI Skills from outside of Microsoft Fabric, these experiments are confined to Python notebooks running within Fabric.
The examples in this repo utilize either Semantic Kernel or Azure AI Agent Service. 

## Using Semantic Kernel

This [Semantic Kernel](https://github.com/microsoft/semantic-kernel)-powered AI Assistant allows you to query your Lakehouse tables and semantic models with [Fabric AI Skills](https://blog.fabric.microsoft.com/en-us/blog/introducing-ai-skills-in-microsoft-fabric-now-in-public-preview/) and [Semantic Link](https://learn.microsoft.com/en-us/fabric/data-science/semantic-link-overview) from within a Microsoft Fabric notebook.
 
To try out the assistant, perform the following steps:
1. [In the Azure Portal, create an Azure AI resource](https://learn.microsoft.com/en-us/azure/ai-services/multi-service-resource?pivots=azportal) and deploy a chat and an embedding model (e.g., gpt-4o and text-embedding-ada-002).
1. In Microsoft Fabric, [Create an AI Skill](https://learn.microsoft.com/en-us/fabric/data-science/how-to-create-ai-skill) and publish it.
1. [Import the notebook into your Fabric workspace](https://learn.microsoft.com/en-us/fabric/data-engineering/how-to-use-notebook#import-existing-notebooks).
1. If your Fabric workspace does not contain a semantic model, download [Retail Analysis Sample PBIX.pbix](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix) and import it to your workspace.
1. Add values to the notebook's parameter cell, incl. Azure AI authentication details and URL of your published AI Skill.
1. Modify the description of the AI Skill Plugin to correspond to the data of your AI Skill.
1. Modify the cell containing the user input to include your query.
1. Run the entire notebook.

## Using Azure AI Agent Service

Note that this version was last updated for version 1.0.0b5 of azure-ai-projects.

In addition to Semantic Kernel, there is now also a notebook using Azure AI Agent Service. This approach allows for the use of built-in capabilities, such as Code Interpreter, as well as custom functions, such as calling an AI Skill. 

To try out the assistant, perform the following steps:
1. Follow the [setup instructions of the Azure AI Agent Service quickstart](https://learn.microsoft.com/en-us/azure/ai-services/agents/quickstart?pivots=programming-language-python-azure).
1. [Create an app registration](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app?tabs=certificate) and give it permissions to the newly created AI resources.
1. In Microsoft Fabric, [Create an AI Skill](https://learn.microsoft.com/en-us/fabric/data-science/how-to-create-ai-skill) and publish it.
1. [Import the notebook into your Fabric workspace](https://learn.microsoft.com/en-us/fabric/data-engineering/how-to-use-notebook#import-existing-notebooks).
1. Add values to the notebook's parameter cell, incl. Azure AI authentication details and URL of your published AI Skill.
1. Modify the doc string of the ```ask_about_data``` function to correspond to the data of your AI Skill.
1. Modify the cell containing the user input to include your query.
1. Run the entire notebook.