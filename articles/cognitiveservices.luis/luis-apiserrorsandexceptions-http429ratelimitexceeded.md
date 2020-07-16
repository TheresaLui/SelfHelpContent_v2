<properties
pageTitle="HTTP 429 Rate Limit Exceeded"
description="HTTP 429 Rate Limit Exceeded"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683903"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_APIsErrorsAndExceptions_HTTPRateLimitExceeded"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# HTTP 429 Rate Limit Exceeded

* For authoring resources and starter keys, LUIS only allows up to 5 transactions per second. You cannot increase this throughput limit.

* For runtime prediction resources, LUIS has two throughput options. 5 transactions/second when using your free tier starter key or F0, and 50 transactions/second with a paid tier S0 subscription key.

* To increase the throughput beyond that, you may assign multiple paid tier keys to your application, and each key will be capable of 50 transactions/second.

## **Recommended Steps**
* Learn about [LUIS Pricing details and the transaction per second(TPS) for each LUIS resource](https://azure.microsoft.com/pricing/details/cognitive-services/language-understanding-intelligent-services/).

* Learn [how to upgrade and assign a paid tier endpoint key to your application here](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#change-pricing-tier).

* Learn more on [common LUIS API response codes](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-response-codes).

* Learn about [LUIS key management experience](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-keys) and the differences between authoring and prediction keys.

* Another option to work around the transaction per second limit is to use [LUIS on containers](https://docs.microsoft.com/azure/cognitive-services/luis/luis-container-howto"). Containers give you the freedom to manage your LUIS application in a connected container environment.
