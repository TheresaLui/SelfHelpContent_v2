<properties
	pageTitle="My bot is slow"
	description="My bot is slow"
	service="Microsoft.BotService"
	resource="botServices"
	authors="arturl,meetshamir"
	ms.author="v-kydela,jaws,arturl,dandris,saziz"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="32689883"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="77fddd59-5718-4315-ac95-12aa65b7be02"
	ownershipId="Compute_BotService"
/>

# My bot is slow

## **Recommended Steps**

  1. Make sure your bot's service code has had time to warm up. If the bot is slow only when initially contacting it, and the bot is hosted on an Azure Web App, consider setting the AlwaysOn option (Note: this could increase the cost of running the bot)
  2. Use the Bot Framework Emulator to connect to your bot's endpoint to see if the problem occurs when talking directly to the bot
  3. Analyze your bot's behavior and see whether the slowness is due to inefficient external calls or queries, or perform high memory/CPU work
  4. If the bot is receiving large volume of traffic, consider scaling it out (Note: this could increase the cost of running the bot)
  5. If your bot is using Direct Line, changing the client to use Web Sockets will improve performance slightly (50-200ms)

## **Recommended Documents**

* [Troubleshoot slow web app performance issues in Azure App Service](https://docs.microsoft.com/azure/app-service/troubleshoot-performance-degradation)<br>
