<properties
	pageTitle="How to create a bot"
	description="How to create a bot"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-kydela,prpillai,hailiu,saziz"
	displayOrder="217"
	selfHelpType="resource"
	supportTopicIds="32688644"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="CD206173-CCDC-4731-B3B7-BC8910C58990"
	ownershipId="Compute_BotService"
/>

# How to create a bot

## **Recommended Steps**
Chat bots can take several forms, such as when an entire bot runs on a webpage in a browser. When we're talking about the Microsoft Bot Framework, we're usually talking about web app bots where the bot code runs in a web app. 

When you create a web app bot you will need a web app to host your bot code, which is handled by an Azure app service resource. You will also need a bot resource which handles bot-specific functionality like the connections between your bot and various bot channels like Microsoft Teams. 

If you use a "Web App Bot" resource as your bot resource then you will have the opportunity to create your bot code from a template when you create the resource, and then you can modify the code in Azure's code editor or you can download the code so you can modify it with your favorite IDE and then republish the code. 

It is also possible to create bot code from a template locally (such as with [these Visual Studio templates](https://marketplace.visualstudio.com/items?itemName=BotBuilder.botbuilderv4)) but you will still need to create the necessary Azure resources when you're ready to deploy the bot.


## **Recommended Documents**

- [Bot creation quickstart](https://docs.microsoft.com/azure/bot-service/abs-quickstart)
- [Bot creation tutorial](https://docs.microsoft.com/azure/bot-service/bot-builder-tutorial-basic-deploy)
