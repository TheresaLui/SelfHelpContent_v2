<properties
	pageTitle="Activities on a channel"
	description="Activities on a channel"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-stkanb,huanchix,egorn,saziz"
	displayOrder="109"
	selfHelpType="resource"
	supportTopicIds="32688616"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="9715117F-04CF-4B05-8F4E-8474B17211A9"
	ownershipId="Compute_BotService"
/>
# I have a problem sending an activity to a channel

## **Recommended Steps**

* Check that the activity type, feature, etc., is supported by the channel it is being sent to. While the Bot Framework may support sending a particular kind of activity (e.g. an adaptive card), some channels may not support receiving them.
* Check that the activity is properly addressed. Message activities sent are usually in response to a message received first, therefore addressing is taken from the inbound activity. Messages sent that are **not** in response to an already received inbound message require a proper *conversational reference* and details about the sender and receiver [[schema](https://docs.microsoft.com/javascript/api/botframework-schema/conversationreference?view=botbuilder-ts-latest), for reference].
* If the issue is related to messaging order, there is no guarantee provided. The Bot Framework attempts to preserve messaging order, however this is channel-specific. The channel is primarily responsible for message delivery and may reorder messages.


## **Recommended Documents**

* [Activity Schema](https://github.com/Microsoft/botframework-sdk/blob/master/specs/botframework-activity/botframework-activity.md)
* [Cards Schema](https://github.com/Microsoft/botframework-sdk/blob/master/specs/botframework-activity/botframework-cards.md)
* [Categorized Activities by Channel](https://docs.microsoft.com/azure/bot-service/bot-service-channels-reference?view=azure-bot-service-4.0)
* [Guide to identifiers (ID fields)](https://docs.microsoft.com/azure/bot-service/bot-service-resources-identifiers-guide?view=azure-bot-service-4.0)
* [Summary of Activities Supported by Channel](https://docs.microsoft.com/azure/bot-service/bot-service-channels-reference?view=azure-bot-service-4.0#summary-of-activities-supported-per-channel)
