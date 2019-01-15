<properties
	pageTitle="My bot is slow"
	description="My bot is slow"
	service="microsoft.bot"
	resource="botservice"
	authors="arturl,meetshamir"
	ms.author="arturl,saziz"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32630643"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# My bot is slow

## **Recommended steps**
  1. Analyze your bot behavior and make sure it doesn’t make inefficient external calls or queries, or perform high memory/CPU work.
  2. If the bot is receiving large volume of traffic, consider scaling it out (Note: it might increase the cost of running the bot).
  3. If your bot is using Direct Line, changing it to use Web Sockets.
  4. If the bot doesn't have AlwaysOn option set, consider setting it (Note: it might increase the cost of running the bot).

## **Recommended documents**
[Troubleshoot slow web app performance issues in Azure App Service](https://docs.microsoft.com/azure/app-service/troubleshoot-performance-degradation)<br>
[Troubleshooting  Bot Timeout Errors](tbd)
