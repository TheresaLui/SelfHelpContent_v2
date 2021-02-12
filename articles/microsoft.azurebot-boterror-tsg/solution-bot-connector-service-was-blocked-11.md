<properties
	pageTitle="Bot connector service endpoint was blocked"
	description="Bot connector service endpoint was blocked"
	service="Microsoft.BotService"
	resource="Microsoft.BotService/botServices"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="766a1780-50fa-4e0b-b7ee-3896ad9ce0c6"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Bot connector service endpoint was blocked

<!--issueDescription-->

1. Bot Connector Services request to post an activity to the bot endpoint was blocked. 
2. Follow the instructions on [Troubleshoot authentication problems](https://docs.microsoft.com/en-us/azure/bot-service/bot-service-troubleshoot-authentication-problems?view=azure-bot-service-4.0)
3. Also check the App Service logs, proxy and firewall settings to ensure that incoming request from the Bot connector service are allowed. 

<!--/issueDescription-->

