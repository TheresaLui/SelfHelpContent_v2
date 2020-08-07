<properties
	pageTitle="Dispatch or Routing"
	description="Dispatch or Routing"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-jewail,jiruss,hailiu,saziz"
	displayOrder="205"
	selfHelpType="resource"
	supportTopicIds="32688640"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="BD6ACAE6-C9D8-4D28-BCB6-F5DC1587E9B2"
	ownershipId="Compute_BotService"
/>

# I need help on Bot Framework SDK Dispatch or Routing

Developers are often required to use different components (parts) to increase their bot intelligence and provide a more natural conversation experience to their customers. Developers include multiple LUIS models, QnA Knowledge Bases and other Azure Cognitive Services to infuse intelligence to their bot.  Bot Builder Dispatch is a tool used evaluate potential intents conflicts and overlap across multiple bot components such as LUIS models and QnA knowledge bases.

Determining which bot component is best suited to handle a given user utterance or provide the best possible answer for any given user query can be challenging. The Dispatch is a component of the new Bot Builder SDKv4 that helps makes bots smarter by using Machine Learning and Natural Language Understanding to determine which part of your bot is best suited to address a user’s given needs.

## **Recommended Steps**

The Dispatch takes representative utterances from your bot’s one or more LUIS models, and QnAMaker knowledge bases to build a machine-learned dispatch model that is used to route requests to the right component. The Dispatch evaluation phase allows you to identify improvements this routing model that can be used to increase your bot overall end-user experience.  The resulting Dispatch LUIS model, created as part of the evaluation phase, is then used to direct incoming utterances to the right LUIS or Q&AMaker Knowledge Base. 

Dispatch is set up with it's own set of CLI tool commands. To understand how to use Dispatch please refer the links below.

## **Recommended Documents**

- [Offical documentation on Dispatch](https://docs.microsoft.com/azure/bot-service/bot-builder-tutorial-dispatch?view=azure-bot-service-4.0&tabs=cs)
- [Dispatch CLI](https://github.com/microsoft/botbuilder-tools/tree/master/packages/Dispatch)
- [Bot sample using dispatch (C#)](https://github.com/microsoft/BotBuilder-Samples/tree/master/samples/csharp_dotnetcore/14.nlp-with-dispatch)
