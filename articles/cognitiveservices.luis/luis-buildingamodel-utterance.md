  <properties
	pageTitle="Utterance "
	description="Utterance "
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683951"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildingAModel_Utterance"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Utterance
## **Recommended Steps**

* [Utterances](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-utterance) are the input examples (sentences) that you use to train your LUIS application. Add utterances that you think users will enter.

* It is important to add [varied utterances of the same meaning in your intent](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-utterance#how-to-choose-varied-utterances) to help LUIS generalize better

* Add [utterances to an intent model](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-add-intents#add-an-example-utterance) you create and [label words in your utterances](https://docs.microsoft.com/azure/cognitive-services/luis/label-entity-example-utterance#label-example-utterances-from-the-intent-detail-page) to extract valuable information from it

* Utterances are meant to be **500 characters long as LUIS** as it is meant to target conversational scenarios only, not long documents

## **Recommended Documents**

* Use [LUIS authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to be able to add utterances from the portal or through APIs

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and if you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f)

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3)
