# Fabric AI Assistant
This [Semantic Kernel](https://github.com/microsoft/semantic-kernel)-powered AI Assistant allows you to query your Lakehouse tables and semantic models with [Fabric AI Skills](https://blog.fabric.microsoft.com/en-us/blog/introducing-ai-skills-in-microsoft-fabric-now-in-public-preview/) and [Semantic Link](https://learn.microsoft.com/en-us/fabric/data-science/semantic-link-overview) - all from within a Microsoft Fabric notebook.
 
To try out the assistant, perform the following steps:
1. [In the Azure Portal, create an Azure AI resource](https://learn.microsoft.com/en-us/azure/ai-services/multi-service-resource?pivots=azportal) and deploy a chat and an embedding model (e.g., gpt-4o and text-embedding-ada-002).
1. In Microsoft Fabric, [Create an AI Skill](https://learn.microsoft.com/en-us/fabric/data-science/how-to-create-ai-skill) and publish it.
1. [Import the notebook into your Fabric workspace](https://learn.microsoft.com/en-us/fabric/data-engineering/how-to-use-notebook#import-existing-notebooks).
1. If your Fabric workspace does not contain a semantic model, download [Retail Analysis Sample PBIX.pbix](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix) and import it to your workspace.
1. Add values to the notebook's parameter cell, incl. Azure AI authentication details and URL of your published AI Skill.
1. Modify the description of the AI Skill Plugin to correspond to the data of your AI Skill.
1. Modify the cell containing the user input to include your query.
1. Run the entire notebook.
