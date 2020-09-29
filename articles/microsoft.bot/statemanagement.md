<properties
	pageTitle="State management"
	description="State management"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="huanchix,hailiu,saziz"
	displayOrder="207"
	selfHelpType="resource"
	supportTopicIds="32688660"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="8A678282-0E75-480A-B955-C139F8B0B705"
	ownershipId="Compute_BotService"
/>

# State management

State within a bot follows the same paradigms as modern web applications, and the Bot Framework SDK provides some abstractions to make state management easier.

## **Recommended Steps**

As with web apps, a bot is inherently stateless; a different instance of your bot may handle any given turn of the conversation. For some bots, this simplicity is preferred - the bot can either operate without additional information, or the information required is guaranteed to be within the incoming message. For others, state (such as where in the conversation we are or previously received data about the user) is necessary for the bot to have a useful conversation.

## **Recommended Documents**

- [Managing state](https://docs.microsoft.com/azure/bot-service/bot-builder-concept-state?view=azure-bot-service-4.0)
- [Save user and conversation data](https://docs.microsoft.com/azure/bot-service/bot-builder-howto-v4-state?view=azure-bot-service-4.0&tabs=csharp)
- [Implement custom storage for your bot](https://docs.microsoft.com/azure/bot-service/bot-builder-custom-storage?view=azure-bot-service-4.0)
- [Manage state data (Warning: v3!)](https://docs.microsoft.com/azure/bot-service/dotnet/bot-builder-dotnet-state?view=azure-bot-service-3.0)
- [Manage custom state data with Azure Cosmos DB for .NET (Warning: v3!)](https://docs.microsoft.com/azure/bot-service/dotnet/bot-builder-dotnet-state-azure-cosmosdb?view=azure-bot-service-3.0)
- [Manage custom state data with Azure Cosmos DB for Node.js (Warning: v3!)](https://docs.microsoft.com/azure/bot-service/nodejs/bot-builder-nodejs-state-azure-cosmosdb?view=azure-bot-service-3.0)
- [Manage custom state data with Azure Table Storage for .NET (Warning: v3!)](https://docs.microsoft.com/azure/bot-service/dotnet/bot-builder-dotnet-state-azure-table-storage?view=azure-bot-service-3.0)
- [Manage custom state data with Azure Table Storage for Node.js (Warning: v3!)](https://docs.microsoft.com/azure/bot-service/nodejs/bot-builder-nodejs-state-azure-table-storage?view=azure-bot-service-3.0)
- [Mange state data (State service deprecation announcement)](https://docs.microsoft.com/azure/bot-service/rest-api/bot-framework-rest-state?view=azure-bot-service-4.0)
