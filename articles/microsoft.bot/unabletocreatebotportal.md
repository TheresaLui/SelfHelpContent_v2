<properties
	pageTitle="Unable to create a bot"
	description="Unable to create a bot"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-stkanb,jiruss,andreo,saziz"
	displayOrder="108"
	selfHelpType="resource"
	supportTopicIds="32688638"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="AD915D5F-EC1E-4235-817C-3A4CAA8505BC"
	ownershipId="Compute_BotService"
/>
# Unable to create a bot

## **Recommended Steps**

* Insufficient permissions may prevent you from creating a bot. You need to have Admin, Contributor, or Owner [RBAC roles](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles) in order to create bots. 
* Your tenant admin may have restricted app registrations. In Azure portal, go to Azure Active Directory -> click on "User Settings" -> verify the following values:

	* Under "App registrations" section, "Users can register applications" should be "Yes";
	* If your account is a guest user, then under "External users" section, "Guest users permissions are limited" should be set to "No"
	
* [The bottroubleshooter community tool](https://github.com/BotBuilderCommunity/botbuilder-community-tools/tree/master/bottroubleshooter) can help identify certain permission issues. Please download the troubleshooter and follow the guidance as detailed in there.
* Bot creation can fail due to network related settings:

	* If you are creating a bot in an Azure ILB ASE, bot creation will fail. Your bot endpoint must be publicly accessible by the Azure Bot Service for creation to succeed. 
	* Check your network settings - if you are on a VPN, try to create the bot without a VPN connection
	* If you are behind a proxy, try it without a proxy

* Bot creation can fail due to browser related settings:

	* Enable third party cookies in your browser. When third party cookies are disabled, bot creation will still succeed but test in web chat will break.
	* Try using InPrivate/InCognito modes, which can help with issues related to browser session/cache
	* Clear the browser cache 

* Enabling App Insights during bot creation can cause issues. Try to create a bot without App Insights, then enable it afterward.
* We recommend the automatic creation of App ID & Password via Azure Portal instead of manual creation. However, if you have to manually create these, please use the new experience available at the [Azure portal](https://ms.portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) and not apps.dev.microsoft.com. More guidance can be found under recommended documents section.

## **Recommended Documents**

* [Create a bot with Azure Bot Service](https://docs.microsoft.com/azure/bot-service/bot-service-quickstart?view=azure-bot-service-4.0)
* [Create and deploy a basic bot](https://docs.microsoft.com/azure/bot-service/bot-builder-tutorial-basic-deploy?view=azure-bot-service-4.0&tabs=csharp%2Cnewrg)
