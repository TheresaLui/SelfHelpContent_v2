<properties
pageTitle="HTTP 404 Operation Not Found"
description="HTTP 404 Operation Not Found"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683902"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_APIsErrorsAndExceptions_HTTPOperationNotFound"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# HTTP 404 or a 410 Operation Not Found

## **Recommended Steps**

### If you get a 404 or a 410 response when using LUIS runtime endpoint
* You may have not published your application yet. [Make sure that you publish your application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-publish-app)

* If you have published your application, make sure [you are using the correct publishing slot](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-publish-app#publishing-slots) whether it is staging or production in the endpoint URL

* If you published to the staging slot, add the query parameter ""&staging=true"" to the URL

### If you get a 404 or a 410 response when using LUIS authoring API
* Make sure you are using the correct authoring URL and parameters

* Sign-in to the [appropriate LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions) you have been authoring your apps in and navigate to [authoring under Azure resources under the manage tab in the top bar](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app)

## **Recommended Documents**

* Learn more on [common LUIS API response codes](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-response-codes)

* [Understand the differences between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-keys)

* Note that response codes may differ if you are using V2 or V3 APIs

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and [V2 Endpoint APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5819c76f40a6350ce09de1ac/operations/5819c77140a63516d81aee78)

* If you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f) and [V3 Endpoint APIs](https://westus.dev.cognitive.microsoft.com/docs/services/luis-endpoint-api-v3-0/operations/5cb0a91e54c9db63d589f433)

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3)
