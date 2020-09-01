  <properties
	pageTitle="Publish Model"
	description="Publish Model"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683930"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildingAModel_publishModel"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Publish Model
###Getting Started

* When you have built your LUIS application and want to use it in a production environment, you need to [publish your application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-publish-app#publishing)

* Publishing packages your application with the intents and entities you have added and provides them behind an endpoint URL that you use to predict your end user's utterances. Integrate this URL with your client application.  

## **Recommended Steps**

* Publishing is still part of your authoring experience. Create an **authoring resource** from the [LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#migration-steps) or from the [Azure portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to build and publish applications.

* [LUIS has 3 authoring regions (US, Europe, Australia) and for each region a corresponding portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions). Location of authoring resource must be the same as the authoring portal region you will be using.

* Note that [publishing regions are tied to authoring regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-regions-are-tied-to-authoring-regions). If your app is currently in the wrong authoring region, export the app, and import it into the correct authoring region for your publishing region.

* To use the endpoint, you need create a **prediction/runtime resource** from [Azure Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-resources-in-the-azure-portal) and [assign it to your application in the LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app)

* After you publish your application, [the LUIS app is published to all regions associated with the LUIS prediction resource added in the LUIS portal.](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions)  

* Understand the [difference between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription)

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and [V2 Endpoint APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5819c76f40a6350ce09de1ac/operations/5819c77140a63516d81aee78)

* If you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f) and [V3 Endpoint APIs](https://westus.dev.cognitive.microsoft.com/docs/services/luis-endpoint-api-v3-0/operations/5cb0a91e54c9db63d589f433)

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3)
