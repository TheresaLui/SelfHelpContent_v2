  <properties
	pageTitle="Accuracy or quality of results"
	description="Accuracy or quality of results"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683884"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildingAModel_accuracyOrQualityOfResults"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Accuracy or quality of results
### Getting Started

* LUIS has several ways to increase the accuracy of your application:
  •	[Adding distinct utterances to different intents](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-utterance#how-to-choose-varied-utterances) to help LUIS generalize better
  •	[Using different types of entities](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-entity-types#types-of-entities) depending on what you want to extract
  •	[Leveraging patterns](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-patterns)
  •	[Use features](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-feature) to define important and significant words in your application and boosts signal of word list
  • [Use the dashboard improve your LUIS app](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-use-dashboard)
  • [Review endpoint utterances](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances) in the LUIS Portal to improve your application over time


## **Recommended Documents**

* [Plan your LUIS application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-plan-your-app) before building it and [identify the intents and entities](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-plan-your-app#identify-your-entities) that you are planning to use. Understand the differences between the both.

* Check the [best practices](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-best-practices#do-and-dont) for building an app in LUIS

* LUIS is non-deterministic, which means results may not be consistent between different training iterations because models are machine learned. You can [make it deterministic by turning off negative sampling](https://docs.microsoft.com/azure/cognitive-services/luis/how-to-application-settings-portal#view-application-name-description-and-id)

* Use [LUIS authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to be able to add increase the accuracy of a LUIS app from the portal or through APIs

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and if you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f)

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3)
