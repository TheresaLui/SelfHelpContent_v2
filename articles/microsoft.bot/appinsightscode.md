<properties
	pageTitle="Configure application insights for Bot SDK code"
	description="Configure application insights for Bot SDK code"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-danava,jiruss,hailiu,saziz"
	displayOrder="213"
	selfHelpType="resource"
	supportTopicIds="32688632"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="E68F818D-B171-4E5B-B37D-D6B10DD0013C"
	ownershipId="Compute_BotService"
/>

# Configure application insights for Bot SDK code

You can enable Application Insights functionality for your bot (App Service) running in Azure, just as you would for other App Services. 

## **Recommended Steps**

Go to your App Service's settings, then to Application Insights. Select `Turn on Application Insights` to enable it. If not created, you have the option to link or create an Application Insights resource. If the App Service (Web App) was created from a **Web App Bot** you *can* use the existing Application Insights resource (already linked to the **Bot Channels Registration**) by clicking on `Turn on Application Insights`.

To fully utilize the Application Insights telemetry and exception logging, you will need to make sure to utilize the appropriate features and functionality from the articles below.

## **Recommended Documents**

- [Add telemetry to your bot](https://docs.microsoft.com/azure/bot-service/bot-builder-telemetry?view=azure-bot-service-4.0)
- [Sample: CoreBot with Application Insights](https://github.com/microsoft/BotBuilder-Samples/blob/master/samples/csharp_dotnetcore/21.corebot-app-insights/README.md)
