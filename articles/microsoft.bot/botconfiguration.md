<properties
	pageTitle="Managing my bot settings"
	description="Managing my bot settings"
	service="Microsoft.BotService"
	resource="botServices"
	authors="v-kydela,sanu-n,meetshamir"
	ms.author="v-kydela,snandan,andreo,saziz"
	displayOrder="104"
	selfHelpType="resource"
	supportTopicIds="32688652"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="1C1B5100-DF66-4A9C-8CBA-979D2B10D8C2"
	ownershipId="Compute_BotService"
/>
# Managing my bot settings

## **Recommended Steps**

### **Managing my bot settings**

In most cases, your bot will have two types of settings:

1. Your bot's **channel registration settings** are used by the Bot Framework's channel connector services to allow your bot to communicate with the chat client applications associated with various channels
1. Your bot's **app configuration settings** are used by the bot itself to determine its own behavior like any other app would, and they can contain useful strings like keys and passwords

### **Managing Channel Registration Settings**

In your **bot resource** in the Azure portal there are two blades where you can configure the way your bot connects to channels: the **Channels** blade and the **Settings** blade.

![Blades](https://i.stack.imgur.com/R5xgh.png)

The Channels blade allows you to decide which channels your bot is connected to and to configure settings that are specific to each of those channels. See [this document](https://docs.microsoft.com/azure/bot-service/bot-service-manage-channels) for more information.

The Settings blade allows you to configure channel-independent bot settings, like the messaging endpoint that channels use to send activities to your bot. If you want to enable [user authentication](https://docs.microsoft.com/azure/bot-service/bot-builder-authentication) with your bot then OAuth connections can also be configured here. See [this document](https://docs.microsoft.com/azure/bot-service/bot-service-manage-settings) for more information.

### **Managing App Configuration Settings**

All apps have app configuration settings so these settings are not necessarily bot-specific, though bots do often rely on these settings to authenticate themselves and access external services for example. An app will generally keep its configuration settings somewhere in its source code files, though the specifics will depend on things like programming languages and frameworks. [ASP.NET Core](https://docs.microsoft.com/aspnet/core/fundamentals/configuration) for example has a variety of possible configuration providers, though it often stores configuration settings in a file called appsettings.json. While you can choose to manage your app configuration settings only in your source code, if your app is deployed to Azure then you can manage them in the Azure portal as well.

The way you access your app configuration settings may depend on the types of Azure resources you create. The two types of bot resources available to you are [Web App Bot](https://docs.microsoft.com/azure/bot-service/abs-quickstart) and [Bot Channels Registration](https://docs.microsoft.com/azure/bot-service/bot-service-quickstart-registration).

**Note**: Functions Bot resources are deprecated and can no longer be created. Microsoft Healthcare Bot resources can be created but they serve a specialized purpose that is beyond the scope of this document.

![Bot resources](https://i.stack.imgur.com/JvjgD.png)

These two bot resource types are almost the same. The idea behind a Web App Bot resource is that your bot is expected to be deployed to an app service in Azure which needs an app service plan, so creating a Web App Bot resource actually creates a whole set of resources. The only difference the individual Web App Bot resource has from a Bot Channels Registration resource is that a Web App Bot resource has three extra blades, and those are used to access the app service that the bot resource is connected to.

**Note**: Azure determines what app service corresponds to your bot resource only by reading the messaging endpoint in your bot resource's Settings blade. If you edit the messaging endpoint so that it doesn't point to an Azure app service domain then you will be unable to access an app service resource through your bot resource. This also means you can edit the messaging endpoint to connect your bot resource to a different app service resource from the one it was originally connected to.

![Build](https://i.stack.imgur.com/55H8U.png)

The **Build** blade is used to access your bot's source code that's been deployed to your app service.

![App Service Settings](https://i.stack.imgur.com/031Nz.png)

The **Configuration** blade is used to access your actual app configuration settings. This blade is the same as the Configuration blade found in your app service resource. The **All App service settings** blade actually opens up your entire app service resource where you can find that same Configuration blade as well as many other blades.

If you're using a Bot Channels Registration resource instead of a Web App Bot resource then these blades won't be available even if your messaging endpoint corresponds to an Azure app service. However, you can still access the app configuration settings by navigating to your app service resource outside of your Bot Channels Registration resource, and you can always edit the configuration directly in your bot code even if your bot code isn't deployed to Azure. Ultimately you get to decide what goes in your app configuration settings because they relate entirely to how you code your app.

### **Troubleshooting Configuration Problems**

If you cannot access your app configuration settings through a Web App Bot resource:

1. Check to make sure your bot's messaging endpoint contains your app service's domain
1. If your app service has been deleted, create a new app service resource and edit your bot's messaging endpoint so that it contains the new app service's domain

If you cannot make edits to Azure resources:

1. Make sure you have the necessary permissions with respect to RBAC (role-based access control)

If you're having other problems in the Azure portal:

1. Try performing a hard refresh with Ctrl+Shift+R or Ctrl+F5 in case there are caching issues
1. Try opening the Azure portal in a new browser window in case the problem is related to a session cookie that's unaffected by hard refreshes
1. Try incognito mode in case the problem is related to multiple accounts being logged incognito
1. Try signing out of Azure and signing back in again in case the problem is related to token expiration
1. Try clearing your cookies

## **Recommended Documents**

- [Manage a bot](https://docs.microsoft.com/azure/bot-service/bot-service-manage-overview)
- [Troubleshoot bot configuration issues](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-bot-configuration)
- [Troubleshooting Bot Framework authentication](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-authentication-problems)
