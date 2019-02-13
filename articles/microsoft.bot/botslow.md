<properties
	pageTitle="My bot is slow"
	description="My bot is slow"
	service="Microsoft.BotService"
	resource="botServices"
	authors="arturl,meetshamir"
	ms.author="arturl,saziz"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="32630658, 32630662, 32630671, 32630675, 32630683, 32630689"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="77fddd59-5718-4315-ac95-12aa65b7be02"
/>

# My bot is slow

## **Recommended Steps**

  1. Analyze your bot behavior and make sure it doesn’t make inefficient external calls or queries, or perform high memory/CPU work
  2. If the bot is receiving large volume of traffic, consider scaling it out (Note: this could increase the cost of running the bot)
  3. If your bot is using Direct Line, change it to use Web Sockets
  4. If the bot doesn't have AlwaysOn option set, consider setting it (Note: this could increase the cost of running the bot)

## **Recommended Documents**

* [Troubleshoot slow web app performance issues in Azure App Service](https://docs.microsoft.com/azure/app-service/troubleshoot-performance-degradation)<br>
* [Troubleshooting  Bot Timeout Errors](tbd)
