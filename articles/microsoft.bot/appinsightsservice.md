<properties
	pageTitle="How to configure application insights for the Bot Service"
	description="How to configure application insights for the Bot Service"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-danava,huanchix,hailiu,saziz"
	displayOrder="219"
	selfHelpType="resource"
	supportTopicIds="32688643"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="1D05C68A-5D8D-487F-B364-81606D50556D"
	ownershipId="Compute_BotService"
/>

# How to configure application insights for the Bot Service

## **Recommended Steps**
If you create a **Web App Bot** or **Bot Channels Registration**, you have the option to create it with an Application Insights resource. If you do so, it will be created, already configured to the Application Insights resource.

If you are not able to create/configure this at creation, you can configure this by going into the **Web App Bot** or **Bot Channels Registration** resource and going to `Settings`. Under analytics, you will see properties for `Application Insights Instrumentation key`, `Application Insights API key` and `Application Insights Application ID`. 

These, respectively, map to the following properties in the Application Insights resource; `Instrumentation Key` (under Overview), `Application ID`  (under API access) and `API key` (not listed/displayed).

Since the API key cannot be retrieved, you can create an new or additional API key if needed. When you create a key, give it a description and then select `Read telemetry` for the permission and the generate the key. Make note of this value and apply these to the values to the appropriate matches under the Web App Bot/Bot Channels Registration settings.

## **Recommended Documents**

- [Add telemetry to your bot](https://docs.microsoft.com/azure/bot-service/bot-builder-telemetry?view=azure-bot-service-4.0)
