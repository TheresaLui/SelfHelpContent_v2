<properties
	pageTitle="Unable to create a bot"
	description="Unable to create a bot"
	service="Microsoft.BotService"
	resource="botServices"
	authors="arturl,meetshamir"
	ms.author="arturl,saziz"
	displayOrder="43"
	selfHelpType="resource"
	supportTopicIds="32630659, 32630663, 32630672, 32630676, 32630684, 32630690, 32630654, 32630666, 32630667, 32630677, 32630679, 32630655, 32630664, 32630665, 32630668, 32630678, 32630686"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="bot-unabletocreatebot"
/>

# Unable to create a bot

Here are the things you can try:

1.	Insufficient permissions may prevent you from creating a bot. You need to have Admin, Contributor or Owner RBAC roles in order to create bots.To understand RBAC roles, please read [this](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles). <br>
	[The bottroubleshooter community tool](https://github.com/BotBuilderCommunity/botbuilder-community-tools/tree/master/bottroubleshooter) can help identify certain permission issues. Please download the troubleshooter and follow the guidance as detailed in there.

2.	Sometimes bot creation can fail due to network related settings:

	1.	Check your network settings, if you are on a VPN try without a VPN connection, if possible.
	2. 	If you are behind a proxy try without a proxy, if possible.

3.	Sometimes bot creation can fail due to browser related settings:
	
	1. 	Enable third party cookies in your browser. When third party cookies are disabled, bot creation will still succeed but test in web chat will break, making one to believe bot creation failed. 
	2. 	Try using InPrivate/InCognito modes, this can help with issues related to browser session/cache.
	3.	Try clearing the browser cache (clearing browser cache removes your browsing history).

4.	Sometimes enabling App Insights during bot creation can cause issues, try and create a bot without App Insights and enable it later on.

5.	If manually creating App ID & Password, we recommend automatic creation of App ID & Password via Azure Portal, however if you have to manually create these please use the new experience available at the [Azure portal](https://ms.portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) and not apps.dev.microsoft.com. More guidance can be found under recommended documents section.


## **Recommended Documents**

* [Create a bot with Azure Bot Service](https://docs.microsoft.com/azure/bot-service/bot-service-quickstart?view=azure-bot-service-4.0)
* [Create and deploy a basic bot](https://docs.microsoft.com/azure/bot-service/bot-builder-tutorial-basic-deploy?view=azure-bot-service-4.0&tabs=csharp%2Cnewrg)

