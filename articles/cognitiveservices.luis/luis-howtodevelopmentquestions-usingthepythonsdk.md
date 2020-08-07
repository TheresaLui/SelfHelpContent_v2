<properties
pageTitle="Using the Python SDK"
description="Using the Python SDK"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683950"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_HowToDevelopmentQuestions_usingThePythonSDK"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Using the Python SDK

## **Recommended Steps**
* Follow the [Python authoring SDK client library quickstart](https://docs.microsoft.com/azure/cognitive-services/luis/sdk-authoring?pivots=programming-language-python) to get started

* Follow the [Python prediction endpoint SDK quickstart](https://docs.microsoft.com/azure/cognitive-services/luis/sdk-query-prediction-endpoint?pivots=programming-language-python)

* Find the [Python SDK reference documentation, samples and PiP packages](https://docs.microsoft.com/azure/cognitive-services/luis/developer-reference-resource#language-based-sdks)

* Understand the [LUIS authoring and prediction requests](https://docs.microsoft.com/azure/cognitive-services/luis/developer-reference-resource#language-understanding-authoring-and-prediction-requests)

* Learn the [difference between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription)

* A common problem with the SDK is that where it requires you to define the Endpoint parameter in the authoring or runtime SDKs, users include /luis/v2.0

* Make sure that when defining the Endpoint parameter it is the custom domain based on the created resource, or the URL based on the location, excluding /luis/v2.0

* Example custom endpoint: https://custom-name.cognitiveservices.azure.com
* Example region endpoint: https://westus.api.cognitive.microsoft.com
