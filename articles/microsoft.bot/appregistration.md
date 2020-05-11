<properties
	pageTitle="Managing my app ID and password"
	description="Managing my app ID and password"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-kydela,jaws,andreo,saziz"
	displayOrder="111"
	selfHelpType="resource"
	supportTopicIds="32688651"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="80BDAA89-90EB-4C9B-A807-C3B7F7FD359F"
	ownershipId="Compute_BotService"
/>
# Managing App registration

### **Managing my app ID and password**

Every bot needs a Microsoft app ID and password in order to identify and authenticate itself when communicating with a client application over a channel. The Microsoft app ID and password are part of a **Microsoft app registration** and are a form of **app credentials**. Microsoft app registrations can serve many purposes beyond just bots: every OAuth connection needs its own app registration for example. Think of an app registration as a way of identifying anything that needs to authenticate itself over the Internet. This document should help you solve issues when working with a Microsoft app registration and its associated app ID and password.

## **Recommended Steps**

### **Creating a Microsoft App Registration**

When you create a **bot resource** (which is a Web App Bot resource or a Bot Channels Registration resource), you have the option of creating the associated app registration automatically. If you want to create an app registration manually you can follow [these steps](https://docs.microsoft.com/azure/bot-service/bot-service-resources-bot-framework-faq#i-need-to-manually-create-my-app-registration-how-do-i-create-my-own-app-registration). Note that if you use the "Create New" option for your app ID and password while creating a bot resource and you enter an app ID and password that are not associated with a Microsoft app registration then your bot resource will be unusable. You cannot create an app registration with a prespecified app ID and password because those values are randomized for you.

### **Editing a Microsoft App Registration**

In the Settings blade of your bot resource, you can click the **Manage** button next to "Microsoft App ID" to be taken to your app registration. There you will be able to create and delete app passwords (called secrets here) in the **Certificates & secrets** blade.

### **Troubleshooting App Registration Problems**

If you cannot find your Microsoft app ID:

1. Check the Settings blade of your bot resource

If you cannot find your Microsoft app password:

1. Check your app configuration settings in your bot's source code
1. If you're using a Web App Bot resource with an associated app service, check the app service's configuration in the Azure portal
1. If you still cannot find your app password, you can create a new one and use that instead

If you cannot access your app registration through your bot resource:

1. Check your [app registrations list](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) to see if the app registration is present
1. If the app registration is not present, please check the account with which you have logged in to Azure portal. There is a possibility that the app was created under a different account.
1. If the app registration has been deleted, you will need to create a new bot resource

## **Recommended Documents**

- [Manage a bot](https://docs.microsoft.com/azure/bot-service/bot-service-manage-overview)
- [ID fields in the Bot Framework](https://docs.microsoft.com/azure/bot-service/bot-service-resources-identifiers-guide)
- [Troubleshooting Bot Framework authentication](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-authentication-problems)
