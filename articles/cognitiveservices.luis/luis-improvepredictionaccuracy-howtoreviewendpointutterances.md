<properties
pageTitle="Review Endpoint Utterances"
description="Understanding how to review endpoint utterances"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683898"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax"
articleId="LUIS_Conversation_ImprovePredictionAccuracy_HowToReviewEndpointUtterances"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Review Endpoint Utterances

## **Recommended Steps**

* Improve your application over time by using [review endpoint utterances](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances) in the LUIS Portal. This is also referred to as the **active learning feature"**.

* Review endpoint utterances from the portal and [select the correct intent and entities](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances#disable-active-learning). Accept these changes into your example utterances then train and publish.

* Active learning captures [endpoint queries](https://docs.microsoft.com/azure/cognitive-services/luis/luis-get-started-create-app#query-the-v2-api-prediction-endpoint) and selects user's endpoint utterances (sentences) that it is unsure of.

* Utterances that are filtered and previewed got **scores for a specific intent between 0.3 and 0.7**. If an utterance did not have a single intent with a score that includes those scores, they will not show up in review endpoint utterances.

* [Enable active learning feature](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances#enable-active-learning) to your application after publishing it.

* [Disable active learning feature](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-review-endpoint-utterances#disable-active-learning) from your application.

* You can export all of your endpoint utterances if you wish to view them.

* Follow the [best practices](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-best-practices#do-and-dont) for building an app in LUIS.
