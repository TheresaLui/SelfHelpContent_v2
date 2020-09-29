<properties
	pageTitle="CLI"
	description="CLI"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-danava,jaws,hailiu,saziz"
	displayOrder="210"
	selfHelpType="resource"
	supportTopicIds="32688627"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="AF60D7AF-D22E-49C3-B1FB-C9F3F0411C25"
	ownershipId="Compute_BotService"
/>

# Bot CLI

The Bot Framework uses a handful of different CLI tools that are used to create, deploy and configure your bot or cognitive services. For creating bot resources in Azure or deploying your bot project to an Azure App Service, the `az` CLI tool is used with the `az bot` command. The `bf` CLI tool is a newer tool that replaces the collection of standalone tools (listed below) used to manage Bot Framework artifacts and related services.

## **Recommended Steps**

- **AZ bot**: Azure CLI tool for creating and deploying Bot resources in Azure
-  **BF**: Newer tool to replace and consolidate the following tools:

	- **Chatdown**: A tool to prototype mock conversations in markdown and convert the markdown to transcripts you can load and view in the new V4 Bot Framework Emulator
 	- **MSBot**: Create and manage connected services in your bot configuration file. Bot files (`*.bot`) are depreciated and this tool is used only for legacy support and management. Will not be included in BF CLI.
 	- **LuDown**: Build LUIS language understanding models using markdown files
 	- **LUIS**: Create and manage your [LUIS.ai](http://luis.ai/) applications
 	- **QnAMaker**: Create and manage [QnAMaker.ai](http://qnamaker.ai/) Knowledge Bases
 	- **Dispatch**: Build language models allowing you to dispatch between disparate components (such as QnA, LUIS and custom code)

## **Recommended Documents**

- [az bot Documentation](https://docs.microsoft.com/cli/azure/bot?view=azure-cli-latest)
- [BF CLI repository](https://github.com/microsoft/botframework-cli/blob/master/README.md)
- [Bot Framework Tools repository](https://github.com/microsoft/botbuilder-tools/blob/master/README.md)
- [Bot Framework CLI overview](https://docs.microsoft.com/azure/bot-service/bf-cli-overview?view=azure-bot-service-4.0)
- [Bot Framework CLI reference](https://docs.microsoft.com/azure/bot-service/bf-cli-reference?view=azure-bot-service-4.0)
- [Deploy your bot](https://docs.microsoft.com/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0&tabs=csharp)

