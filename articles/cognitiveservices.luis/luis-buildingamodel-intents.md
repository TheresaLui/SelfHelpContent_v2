  <properties
	pageTitle="How to Build a Model using intents in LUIS"
	description="How to Build a Model using intents in LUIS"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683907"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildAModel_Intents"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# How to Build a Model using intents in LUIS
### Getting Started

* [Intents in LUIS](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-intent) allow you to identify the objective of a sentence. Train Intents by adding [example utterances(sentences)](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-utterance) to an Intent.

* It is important to add **varied utterances of the same meaning in your intent** to help LUIS generalize better. For example, a "Cancel" intent would include example utterances such as I would like to cancel my subscription, please cancel that action and stop the current action.

* To better resolve more details in the intent, use [entities](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-entity-types) to capture or extract details like "what" you are cancelling

## **Recommended Steps**

* You first need to [plan your LUIS application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-plan-your-app) before building it and [identify the intents and entities](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-plan-your-app#identify-your-entities) that you are planning to use. Understand the differences between both intents and entities.

* Learn how to [add an intent to your LUIS app](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-add-intents#add-an-intent-to-your-app)

* An [intent prediction error](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-add-intents#intent-prediction-errors) can occur while building your application after your first train. This is determined when the utterance is not predicted with the trained app for the intent and helps you debug your model while creating your application.

* Intents are mutually exclusive, which means their [scores are on a scale of 0 to 1 independently of each other](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-intent#return-all-intents-scores)

* Two LUIS intents can have high scores for the same utterance if they use a lot of the same vocabulary

* If a specific utterance is not getting matched as the expected top intent, then [use the Analytics Dashboard](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-use-dashboard) to obtain [actionable advice on weak intents](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-use-dashboard#intents-with-errors) from the dashboard

* It would be likely that there is another intent that contains utterances with several of the same words of the utterance getting incorrectly detected. The Analytics Dashboard will help identify which intents are conflicting.

## **Recommended Documents**

* The [None intent](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-intent#none-intent) is created when you first create your LUIS application but is left empty on purpose to fill it with utterances that are outside of your domain. The is required and **can't be deleted or renamed**.

* You can [import prebuilt intents and its utterances](https://docs.microsoft.com/azure/cognitive-services/LUIS/howto-add-prebuilt-models#add-a-prebuilt-intent) and modify it to tailor your needs

* Learn what is meant by [intent balance](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-intent#intent-balance) and best practices of using intents

* Learn about the [LUIS model limits](https://docs.microsoft.com/azure/cognitive-services/luis/luis-limits#model-boundaries)

* Check the [best practices](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-best-practices#do-and-dont) for building an app in LUIS

* Use [LUIS authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to be able to add intents from the portal or through APIs

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and if you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f)

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3)
