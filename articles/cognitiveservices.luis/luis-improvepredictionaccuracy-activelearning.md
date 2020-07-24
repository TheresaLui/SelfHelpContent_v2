<properties
pageTitle="Active Learning"
description="Work with active Learning"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683885"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_ImprovePredictionAccuracy_ActiveLearning"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Active Learning

## **Recommended Steps**

* Improve your application over time by using [review endpoint utterances](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances) in the LUIS Portal. This is also referred to as the **active learning feature"**.

* Active learning captures [endpoint queries](https://docs.microsoft.com/azure/cognitive-services/luis/luis-get-started-create-app#query-the-v2-api-prediction-endpoint) and selects user's endpoint utterances (sentences) that it is unsure of.

* Utterances that are filtered and previewed got **scores for a specific intent between 0.3 and 0.7**. If an utterance did not have a single intent with a score that includes those scores, they will not show up in review endpoint utterances.

* [Enable active learning feature](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances#enable-active-learning) to your application after publishing it.

* Review endpoint utterances from the portal and [select the correct intent and entities](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances#disable-active-learning). Accept these changes into your example utterances then train and publish.

* [Disable active learning feature](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances#disable-active-learning) from your application.

* Export all your endpoint utterances if you wish to view them [programmatically](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5ae02c03d5b81c092c6cf2c2) or from LUIS portal in the "My Apps" page by selecting the application and **export endpoint logs** from the top toolbar.  

* Use the [LUIS analytics dashboard](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-use-dashboard) to give you an overview of your **training data's accuracy** and help you improve your LUIS app.

* Read [this tutorial](https://docs.microsoft.com/azure/cognitive-services/luis/luis-tutorial-review-endpoint-utterances#review-endpoint-utterances) to fix unsure predictions by reviewing endpoint utterances.

* Follow the [best practices](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-best-practices#do-and-dont) for building an app in LUIS.
