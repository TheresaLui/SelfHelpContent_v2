  <properties
	pageTitle="Entity"
	description="Entity"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683894"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildingAModel_Entity"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Entity
### Getting Started

* [Entities in LUIS](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-entity-types) allow you to extract information from a sentence

* There are [multiple different entity types](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-entity-types#types-of-entities) that allow you to extract information in different ways

## **Recommended Steps**

* You first need to [plan your application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-plan-your-app) before building it and [identify the intents and entities](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-plan-your-app#identify-your-entities) that you are planning to use

* Depending on what you want to extract from your [utterances](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-utterance), choose the type of entity that will work with it

## **Recommended Documents**

* [**Machine-learned (ML) entities**](https://docs.microsoft.com/azure/cognitive-services/luis/reference-entity-machine-learned-entity?tabs=V3) is the preferred entity for building LUIS applications because of its [decomposability feature](https://docs.microsoft.com/azure/cognitive-services/luis/tutorial-machine-learned-entity#entity-decomposability-is-important)

* If an utterance with an expected entity is not getting correctly extracted, consider adding an example closely similar to it with a few variations, in order to train the entity extractor with that specific pattern or sequence of words

* Learn how to easily [create machine learned entities](https://docs.microsoft.com/azure/cognitive-services/luis/tutorial-machine-learned-entity#create-machine-learned-entity) and [label utterances](https://docs.microsoft.com/azure/cognitive-services/luis/tutorial-machine-learned-entity#label-example-utterances)

* Add [phrase list features](https://docs.microsoft.com/azure/cognitive-services/luis/tutorial-machine-learned-entity#edit-subentities-to-improve-extraction) to improve prediction accuracy of entity and [configure them as required features](https://docs.microsoft.com/azure/cognitive-services/luis/tutorial-machine-learned-entity#configure-required-features)

* Read [this tutorial](https://docs.microsoft.com/azure/cognitive-services/luis/tutorial-machine-learned-entity) for best practices on how to use ML entities

* [**List entities**](https://docs.microsoft.com/azure/cognitive-services/luis/reference-entity-list?tabs=V2) allow you to define a list of words and their synonyms to exact match. **Use it when** text data is a known set and does not change a lot.

* [**Regex entities**](https://docs.microsoft.com/azure/cognitive-services/luis/reference-entity-regular-expression?tabs=V2) allow you to define regular expressions to extract specific patterns from your utterances. **Use it when** text data is consistently formatted with any variation that is also consistent.

* [**Pattern.any entity**](https://docs.microsoft.com/azure/cognitive-services/luis/reference-entity-pattern-any?tabs=V2)is a variable-length placeholder used only in a [pattern's](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-patterns#patternany-entity) template utterance to mark where the entity begins and ends. This entity[need to be marked in the Pattern template examples](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-model-intent-pattern), not the intent user examples. **Use it when** the ending of the entity can be confused with the remaining text of the utterance.

* [**Prebuilt entities**](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-prebuilt-model#prebuilt-entities) are out-of-the-box entity extractors that you do not have to define yourself. You add them and it [extracts common information](https://docs.microsoft.com//azure/cognitive-services/luis/luis-reference-prebuilt-entities#english-american-entity-support) such as numbers, dates, times, currency, emails, and more.

### Things to Note

* You will not be able to create simple or composite entities anymore as these have been replaced by machine learned entities. It is also encouraged to upgrade to machine-learning entity. Please read the [following instructions and limitations carefully before upgrading](https://docs.microsoft.com/azure/cognitive-services/luis/migrate-from-composite-entity).

* Note that if you export an application from the portal (uses V3 APIs) and try to import it back programmatically using V2 APIs, import will fail as it is not forward compatible

* Patterns primarily work for intents only and not entities. Pattern.any extracts information from the pattern. It will check if the entity is extracted then check if the pattern around it matches, go to the specific intent.
