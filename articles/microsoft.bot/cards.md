<properties
	pageTitle="Cards"
	description="Cards"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-kydela,jiruss,hailiu,saziz"
	displayOrder="209"
	selfHelpType="resource"
	supportTopicIds="32688625"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="A196636D-FB02-461F-8526-6819A48887D8"
	ownershipId="Compute_BotService"
/>

# Cards

The Microsoft Bot Framework defines a handful of "rich cards" (or just "cards") like hero cards, receipt cards, and animation cards. [Adaptive Cards](https://blog.botframework.com/2019/07/02/using-adaptive-cards-with-the-microsoft-bot-framework/) are also generally counted as rich cards though Adaptive Cards have been developed as their own project outside of the Bot Framework. Cards are meant to be attached to messages that a bot sends to a user so that they can be rendered by the chat client

## **Recommended Steps**

Depending on the type of card you use, cards can contain a combination of display elements and interactive components that often provide a better user experience than just plain text. When you attach a card to a message, the Bot Framework channel connector services will try to interpret the card in a way that applies to whatever API the channel provides, so Slack or Facebook Messenger for example will be able to render Bot Framework cards according to their own respective platforms. Because the Bot Framework depends on each channel's client applications to actually render the cards, [card behavior is entirely channel-dependent](https://docs.microsoft.com/azure/bot-service/bot-service-channels-reference#card-support-by-channel) and you should always make sure to test every card you plan to use on every channel you plan to connect your bot to.

## **Recommended Documents**
- [Cards overview](https://github.com/Microsoft/botframework-sdk/blob/master/specs/botframework-activity/botframework-cards.md)
- [How to develop a bot that uses cards](https://docs.microsoft.com/azure/bot-service/bot-builder-howto-add-media-attachments)
- [Bot Framework schema reference](https://docs.microsoft.com/azure/bot-service/rest-api/bot-framework-rest-connector-api-reference#schema)

