<properties
pageTitle="HTTP 400 Invalid Request"
description="HTTP 400 Invalid Request"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683900"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_APIsErrorsAndExceptions_HTTPInvalidRequest"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# HTTP 400 Invalid Request

## **Recommended Steps**

### If you get a 400 response when using LUIS runtime endpoint
* Make sure that the request's parameters are correct meaning the required parameters are not missing or malformed.

### If you get a 400 response when using LUIS authoring API
* Every invalid request should return with a message explaining why the request is invalid and suggests a way to resolve it.

* Learn more on [common LUIS API response codes](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-response-codes).

* Learn about [LUIS key management experience](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-keys) and the differences between authoring and prediction keys.

* Note that response codes may differ if you are using V2 or V3 APIs.

* If you are using LUIS V2 APIS, review LUIS [V2 Authoring APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f) and [V2 Endpoint APIs](https://westus.dev.cognitive.microsoft.com/docs/services/5819c76f40a6350ce09de1ac/operations/5819c77140a63516d81aee78).

* If you are using LUIS V3 APIS, review LUIS [V3 Authoring APIs](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f) and [V3 Endpoint APIs](https://westus.dev.cognitive.microsoft.com/docs/services/luis-endpoint-api-v3-0/operations/5cb0a91e54c9db63d589f433).

* Learn how to [migrate to V3 APIs](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-api-v3).
