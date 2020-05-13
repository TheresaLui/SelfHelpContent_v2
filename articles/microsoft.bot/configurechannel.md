<properties
	pageTitle="Cannot configure a channel"
	description="Cannot configure a channel"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-kydela,jiruss,egorn,saziz"
	displayOrder="110"
	selfHelpType="resource"
	supportTopicIds="32688624"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="E5DC946E-0FB9-40D6-B0EA-351D3C8AF16D"
	ownershipId="Compute_BotService"
/>
# Cannot configure a channel

## **Recommended Steps**

You can connect your bot to different channels by accessing the Channels blade in your bot resource:

![Channels blade](https://docs.microsoft.com/azure/bot-service/media/channels/connect-to-channels.png?view=azure-bot-service-4.0)

### **Troubleshooting Channel Configuration Problems**

When you click on a channel to configure it in your Channels blade:

* If you see the error message "The resource you are looking for has been removed, had its name changed, or is temporarily unavailable.", this is currently a bug with the Direct Line Speech channel that some users encounter. Unfortunately there is not a mitigation at this time other than to try a different Azure account.

* If the frame for the channel loads but it says you're not authorized to configure that channel for your bot, this could mean the owner of your Azure directory needs to give you permission to use that channel. This can happen with the Cortana channel.

* For other problems that are related to a specific channel, you can find channel-specific information for each channel in the [Azure Bot Service Documentation](https://docs.microsoft.com/azure/bot-service/?view=azure-bot-service-4.0) under How-To > Manage > Channels. The configuration page for each channel in the Channels blade in the Azure portal also links directly to that channel's document.

## **Recommended Documents**

* [Connect a bot to channels](https://docs.microsoft.com/azure/bot-service/bot-service-manage-channels)
* [Troubleshoot bot configuration issues](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-bot-configuration)

