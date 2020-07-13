<properties
pageTitle="LUIS returns wrong intent"
description="LUIS returns wrong intent"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683911"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax"
articleId="LUIS_Conversation_ImprovePredictionAccuracy_LUIS returns wrong intent"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# LUIS returns wrong intent

* Understand the [prediction scores that are used in LUIS along with their confidence](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-prediction-score).

* You can [return prediction score for all intents](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-prediction-score#return-prediction-score-for-all-intents) to review the intents with similar scores and try to issues of intents with similar scores.

## **Recommended Steps**

* Continue to add utterances to each intent with a wider variety of contextual differences or you can have the client application, such as a chat bot, make programmatic choices about how to handle the 2 top intents.

* The 2 intents, which are too-closely scored, may invert due to [non-deterministic training](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-prediction-score#return-prediction-score-for-all-intents). You can try [turning off non-deterministic training](https://docs.microsoft.com/azure/cognitive-services/luis/how-to-application-settings-portal#view-application-name-description-and-id).

* You can improve your application over time by using [review endpoint utterances](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances) in the LUIS Portal.

* Read [this tutorial](https://docs.microsoft.com/azure/cognitive-services/luis/luis-tutorial-review-endpoint-utterances#review-endpoint-utterances) to fix unsure predictions.

* You can use [patterns to make the correct intent's score significantly higher](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-patterns) in percentage and farther from the next highest score.

* Read [best practices](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-best-practices#do-and-dont) for building an app in LUIS.
