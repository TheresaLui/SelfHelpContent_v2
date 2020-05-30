<properties
	pageTitle="I have a problem with a channel"
	description="I have a problem with a channel"
	service="Microsoft.BotService"
	resource="botServices"
	authors="arturl,meetshamir"
	ms.author="arturl,saziz"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32688622"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="72372ddb-82ce-4172-af6f-4d616a3844ff"
	ownershipId="Compute_BotService"
/>

# I have a problem with a channel

## **Recommended Steps**

1. [Test Your Bot In Web Chat](https://docs.microsoft.com/azure/bot-service/bot-service-quickstart?view=azure-bot-service-4.0#test-the-bot-1). This will allow you to determine if the problem is specific to your bot (bot doesn't work in any channel), or to a particular channel (bot works in some channels but not others).
2. If the bot doesn't respond in Web Chat, make sure the bot application is running. In the "Overview" blade, copy the Messaging endpoint and paste it into your browser. If the endpoint returns an error "This site can't be reached" or "can't reach this page", that means that your bot is down and you need to redeploy it.
3. If the endpoint returns HTTP Error 405, it means the bot is reachable and the bot is able to respond to messages. You should investigate whether your bot times out or [fails with an HTTP 5xx error](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-500-errors?view=azure-bot-service-4.0&tabs=dotnetwebapi).
4. If the bot works as expected in Web Chat but fails in some other channel, possible reasons are:

	* **Channel Configuration Issues**: Determine if channel configuration parameters have been set incorrectly or have changed externally. Try removing the channel and redoing the channel configuration with the right parameters.
	* **Channel-Specific Behavior**: Determine if a feature you're using is supported by the channel. If you see differences in how some message types work in different channels, consult [Connect a bot to channels](https://docs.microsoft.com/azure/bot-service/bot-service-manage-channels).
	* **Channel Outage**: Determine if the channel you're using is experiencing an outage. This can be done by consulting a channel website (see below) or by building a test echo bot and connecting it to the channel.

## **Recommended Documents**

* [Test Your Bot In Web Chat](https://docs.microsoft.com/azure/bot-service/bot-service-quickstart?view=azure-bot-service-4.0#test-the-bot-1)
* [Connect a bot to channels](https://docs.microsoft.com/azure/bot-service/bot-service-manage-channels)
* [Implement channel-specific functionality](https://docs.microsoft.com/azure/bot-service/bot-builder-channeldata?view=azure-bot-service-4.0)
* Third Party Channel Availability:

  * [Facebook Platform](https://developers.facebook.com/status/dashboard/)<br>
  * [Slack System Status](https://status.slack.com/)<br>
  * [Telegram Twitter feed](https://twitter.com/telegram)<br>
  * [Twilio Status](https://status.twilio.com/)<br>
  * [Kik Twitter feed](https://twitter.com/Kik)<br>
