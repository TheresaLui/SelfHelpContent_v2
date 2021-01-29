<properties
pageTitle="LUIS key management errors"
description="LUIS key management errors"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683910"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_APIsErrorsAndExceptions_LUISKeyManagementErrors"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# LUIS Key Management Errors
### Getting Started

* Understand all types of resources offered by LUIS [here](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#luis-resources).

* When creating a LUIS account, a starter key is automatically generated for the account for a non-migrated users.

* A new users will require to associate their LUIS application with a [F0 authoring resource key](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal).

* The **F0 authoring key** and the **starter key** allow up to 1 million calls to LUIS authoring/programmatic APIs a month and allow up to 1000 endpoint calls a month.

* Associate your LUIS applications with the [F0 prediction key](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app) to allow up to 10,000 endpoint calls a month. If you need more, purchase the [S0 prediction key](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#change-pricing-tier).  

## **Recommended Steps**

* If you are getting a **403 quota exceeded response** and using a key, you have exceeded the F0 authoring quota or the F0 prediction quota and it will be replenished at the beginning of next month  

* Use Azure portal to check [how many transactions a key has made](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#viewing-azure-resource-metrics)

* To exceed the endpoint calls per month, [purchase a LUIS paid tier (S0) runtime key through Azure](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#change-pricing-tier) and [assign it to your application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app)

* Learn about [LUIS Pricing details and the transaction per second(TPS) for each key](https://azure.microsoft.com/pricing/details/cognitive-services/language-understanding-intelligent-services/)

* Learn about [LUIS resource boundaries and key tiers](https://docs.microsoft.com/azure/cognitive-services/luis/luis-boundaries#key-limits)

* [**Understand the differences between authoring and prediction keys**](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-keys)

* Note that response codes may differ if you are using V2 or V3 APIs

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and [V2 Endpoint APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5819c76f40a6350ce09de1ac/operations/5819c77140a63516d81aee78)

* If you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f) and [V3 Endpoint APIs](https://westus.dev.cognitive.microsoft.com/docs/services/luis-endpoint-api-v3-0/operations/5cb0a91e54c9db63d589f433)

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3)
