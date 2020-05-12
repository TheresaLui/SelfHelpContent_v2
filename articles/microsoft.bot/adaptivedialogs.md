<properties
	pageTitle="Adaptive Dialogs"
	description="Adaptive Dialogs"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-kydela,jaws,hailiu,saziz"
	displayOrder="206"
	selfHelpType="resource"
	supportTopicIds="32688617"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="2B99D869-59FB-4A0F-9B72-76F3C2E6265F"
	ownershipId="Compute_BotService"
/>

# Bot Framework SDK Adaptive Dialogs

Adaptive dialogs provide a new way to easily and dynamically define the flow of your bot's conversation. Like a waterfall dialog, an Adaptive dialog is composed of steps but instead of being functions these steps are themselves dialogs, nested inside the Adaptive dialog. While Adaptive dialogs are still in preview, you can try out the [Adaptive dialogs NuGet package](https://www.nuget.org/packages/Microsoft.Bot.Builder.Dialogs.Adaptive) for your .NET bots.

## **Recommended Steps**

Adaptive dialogs can be defined using a [declarative syntax](https://github.com/microsoft/BotBuilder-Samples/tree/master/experimental/adaptive-dialog/declarative) that can then be consumed by your bot, so you can write your dialogs without using actual C# code. These "declarative dialogs" can be easily created using the UI-based [Bot Framework Composer](https://github.com/microsoft/BotFramework-Composer) (also in preview).

## **Recommended Documents**

- [Adaptive dialogs overview](https://github.com/microsoft/BotBuilder-Samples/tree/master/experimental/adaptive-dialog)
- [Adaptive dialogs source code](https://github.com/microsoft/botbuilder-dotnet/tree/master/libraries/Microsoft.Bot.Builder.Dialogs.Adaptive)
