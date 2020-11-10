  <properties
	pageTitle="Training"
	description="Training"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683940"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildingAModel_Training"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Training
### Getting Started

* [Training your LUIS app](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-train) is the teaching action that uses all the examples you have defined in your app including the intent classifiers and entity extractors

* Training and testing an app is an **iterative process**. After you train your LUIS app, you test it with sample utterances to see if the intents and entities are recognized correctly. If they're not, make updates to the LUIS app, then train, and test again.

## **Recommended Steps**

* Sometimes, results differ between one train and the other. This is because [LUIS training is non-deterministic](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-train#train-with-all-data). In LUIS there is no way to provide negative examples, so LUIS uses negative sampling where it takes random examples from other intents and uses them as negative examples for the intent you're training.

* To turn off negative sampling, and use all your training data as negative examples, [change the application settings](https://docs.microsoft.com/azure/cognitive-services/luis/how-to-application-settings-portal#view-application-name-description-and-id)

## **Recommended Documents**

* Use [LUIS authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to be able to train from the portal or through APIs

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and if you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f)

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3)
