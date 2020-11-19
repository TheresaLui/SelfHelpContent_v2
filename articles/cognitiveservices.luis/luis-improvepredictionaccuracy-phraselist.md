<properties
pageTitle="Phrase List"
description="Phrase List"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683922"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_ImprovePredictionAccuracy_PhraseList"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Phrase list or Features
* [Features](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-feature) were previously referred to as phrase lists

* Adding features allows you to define important and significant words in your application and boosts signal of word list

* Features give higher weights to the words that are included in it, therefore give higher scores when they appear. Adding them properly to you application helps improving its prediction accuracy.

* Many get confused on when to use phrase list features list entities. [List entities](https://docs.microsoft.com/azure/cognitive-services/luis/reference-entity-list?tabs=V2) are a list of words that get extracted exactly as they are in the list entity. They are used differently to phrase list features, which tend to improve your model as a whole.

* List entity synonyms do not affect your intent or entity predictions unless you add them as a feature to the intent or entity

## **Recommended Steps**

* Review concepts of [phrase list feature](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-feature#a-phrase-list-for-a-particular-concept), [model as a feature](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-feature#a-model-as-a-feature-helps-another-model), [required features](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-feature#required-features) and [global features](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-feature#global-features) and understand when to use each

* Learn how to add [phrase list as a feature](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-add-features#add-phrase-list-as-a-feature)

* Learn how to add [model as a feature](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-add-features#model-as-a-feature)

* Follow the [best practices](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-best-practices) for building an app in LUIS to understand how to use features in the cycle of creating an app
