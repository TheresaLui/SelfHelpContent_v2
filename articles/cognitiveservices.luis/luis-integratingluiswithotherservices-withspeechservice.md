<properties
pageTitle="With Speech Service"
description="With Speech Service"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683956"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_integratingLUISWithOtherServices_withSpeechService"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# With Speech Service

## **Recommended Steps**

* You can easily integrate the [Cognitive Speech Services](https://azure.microsoft.com/services/cognitive-services/speech-services/) with LUIS
to recognize intents from speech.

* [You only need a LUIS resource to integrate with speech](https://docs.microsoft.com/azure/cognitive-services/speech-service/how-to-recognize-intents-from-speech-csharp?toc=/azure/cognitive-services/luis/toc.json&bc=/azure/cognitive-services/luis/breadcrumb/toc.json). You will not need a speech resource.

* This integration allows you to make audio requests and retrieve LUIS responses, which improves latency

* The Speech model uses the utterances in your LUIS application to improve the speech to text accuracy

* [Install the Speech SDK](https://docs.microsoft.com/azure/cognitive-services/speech-service/how-to-recognize-intents-from-speech-csharp?toc=/azure/cognitive-services/luis/toc.json&bc=/azure/cognitive-services/luis/breadcrumb/toc.json#install-the-speech-sdk) and [create a speech project](https://docs.microsoft.com/azure/cognitive-services/speech-service/how-to-recognize-intents-from-speech-csharp?toc=/azure/cognitive-services/luis/toc.json&bc=/azure/cognitive-services/luis/breadcrumb/toc.json#create-a-speech-project-in-visual-studio) in visual studio

* Learn more about this integration by [following this tutorial](https://docs.microsoft.com/azure/cognitive-services/speech-service/how-to-recognize-intents-from-speech-csharp?toc=/azure/cognitive-services/luis/toc.json&bc=/azure/cognitive-services/luis/breadcrumb/toc.json)
