<properties
pageTitle="Adding Pattern"
description="Adding Pattern"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683886"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_ImprovePredictionAccuracy_AddingPattern"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Adding Pattern

### Getting Started

*  When the scores of the two top intents are close, use [patterns to make the correct intent's score significantly higher](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-patterns) in percentage and farther from the next highest score.

* A pattern is applied as a combination of text matching and machine learning.

* Patterns match specific [templates utterances](https://docs.microsoft.com/azure/cognitive-services/luis/luis-tutorial-pattern#template-utterances) to intents. The template utterance in the pattern, along with the example utterances in the intent, give LUIS a better understanding of what utterances fit the intent.

* If you include an entity in a template utterance, that means the entity must be extracted first, and then the rest of the template will be detected. If you want to match an entity based on the template, use a [Pattern.any entity](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-patterns#patternany-entity).


## **Recommended Steps**

* Create template for an utterance by [learning pattern syntax](https://docs.microsoft.com/azure/cognitive-services/luis/reference-pattern-syntax).

* Follow the [best practices](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-best-practices#do-and-dont) for building an app in LUIS.
