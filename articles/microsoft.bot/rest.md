<properties
	pageTitle="REST API"
	description="EEST API"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-kydela,prpillai,hailiu,saziz"
	displayOrder="211"
	selfHelpType="resource"
	supportTopicIds="32688633"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="BD92219F-7C44-45BE-A44F-8A9B9F8F3F72"
	ownershipId="Compute_BotService"
/>

# Connector or REST API

The Microsoft Bot Framework's connector services are accessed using the Bot Framework REST API. This API consists of a handful of operations that bots can use to interact with the bot channel, such as by sending a message to a user.

## **Recommended Steps**

While you can call the REST API directly with your preferred HTTP client, bots built with the Bot Builder SDK are expected to access the REST API indirectly by using the Bot Connector library (available in several programming languages like [C#](https://www.nuget.org/packages/Microsoft.Bot.Connector/) and [JavaScript](https://www.npmjs.com/package/botframework-connector)). In most cases you won't even need to use the Bot Connector library directly, since its functionality can be accessed through Bot Builder objects like bot adapters and turn contexts.

## **Recommended Documents**

- [Bot Framework REST API overview](https://docs.microsoft.com/azure/bot-service/rest-api/bot-framework-rest-overview)
- [Bot Framework REST API reference](https://docs.microsoft.com/azure/bot-service/rest-api/bot-framework-rest-connector-api-reference)
