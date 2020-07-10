<properties
	pageTitle="Middleware"
	description="Middleware"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-micric,prpillai,hailiu,saziz"
	displayOrder="207"
	selfHelpType="resource"
	supportTopicIds="32688653"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="8116E9D7-9D90-4319-8F54-F0F76173DA9E"
	ownershipId="Compute_BotService"
/>

# Middleware

Middleware is simply a class that sits between the adapter and your bot logic, added to your adapter's middleware collection during initialization. The SDK allows you to write your own middleware or add middleware created by others. Every activity coming into or out of your bot flows through your middleware.

The adapter processes and directs incoming activities in through the bot middleware pipeline to your bot’s logic and then back out again. As each activity flows in and out of the bot, each piece of middleware can inspect or act upon the activity, both before and after the bot logic runs.

## **Recommended Steps**

Before starting coding for middleware, it is important to understand [bots in general](https://docs.microsoft.com/azure/bot-service/bot-builder-basics?view=azure-bot-service-4.0) and [how they process activities](https://docs.microsoft.com/azure/bot-service/bot-builder-basics?view=azure-bot-service-4.0#the-activity-processing-stack).
After that please use the links in the below section for further information.

## **Recommended Documents**

- [Middleware Docs](https://docs.microsoft.com/azure/bot-service/bot-builder-concept-middleware?view=azure-bot-service-4.0)
- [StackOverflow](https://stackoverflow.com/search?q=%5Bbotframework%5D+middleware)
