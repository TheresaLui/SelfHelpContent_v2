  <properties
	pageTitle="Building a model using REST APIs"
	description="Building a model using REST APIs"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683890"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildingAModel_buildingAModelUsingRESTAPIs"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Building a model using REST APIs
### Getting Started

* LUIS is built on a set of REST APIs that can be easily integrated in a wider solution. LUIS offers an SDK that packages these APIs in a simple to use manner.

* You can fully automate authoring a LUIS model using the APIs with your [LUIS Authoring Resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#luis-resources)

* Create a new authoring resource either from the [LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#migration-steps) or from the [Azure portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal)

* **Make sure it is an authoring and not a runtime/prediction LUIS resource**. Learn the [difference between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription).

* If you are an existing LUIS user, you will need to first [Migrate your account](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#what-is-migration) to link your authoring resource to your LUIS account


## **Recommended Documents**

* Use [LUIS authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to be able to increase the accuracy of a LUIS app from the portal or through APIs

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and if you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f)

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3
