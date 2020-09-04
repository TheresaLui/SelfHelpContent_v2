<properties
pageTitle="Using the Java SDK"
description="Using the Java SDK"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683948"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_HowToDevelopmentQuestions_usingTheJavaSDK"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Using the Java SDK

## **Recommended Steps**

* Find the [Java SDK reference documentation and Maven packages](https://docs.microsoft.com/azure/cognitive-services/luis/developer-reference-resource#language-based-sdks)

* Follow the [Java SDK Samples for LUIS](https://github.com/Azure-Samples/cognitive-services-java-sdk-samples/tree/master/Language/LanguageUnderstanding)

* Understand the [LUIS authoring and prediction requests](https://docs.microsoft.com/azure/cognitive-services/luis/developer-reference-resource#language-understanding-authoring-and-prediction-requests)

* Learn the [difference between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription)

* A common problem with the SDK is that where it requires you to define the Endpoint parameter in the authoring or runtime SDKs, users include /luis/v2.0

* Make sure that when defining the Endpoint parameter it is the custom domain based on the created resource, or the URL based on the location, excluding /luis/v2.0

* Example custom endpoint: https://custom-name.cognitiveservices.azure.com
* Example region endpoint: https://westus.api.cognitive.microsoft.com
