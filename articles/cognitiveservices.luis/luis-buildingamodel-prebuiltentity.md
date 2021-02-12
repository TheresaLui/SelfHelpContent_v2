  <properties
	pageTitle="Prebuilt Entity"
	description="Prebuilt Entity"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683927"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildingAModel_prebuiltEntity"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Prebuilt Entity

* [**Prebuilt entities**](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-prebuilt-model#prebuilt-entities) are out-of-the-box entity extractors that you do not have to define yourself. You add them and it [extracts common information](https://docs.microsoft.com//azure/cognitive-services/luis/luis-reference-prebuilt-entities#english-american-entity-support) such as numbers, dates, times, currency, emails, and more.

* Prebuilt entities use [Microsoft's open source Text-Recognizers](https://github.com/Microsoft/Recognizers-Text). Prebuilt entities are automatically matched through a mix of regular expressions. You cannot remove their labels because they will always be predicted within LUIS.


## **Recommended Steps**

* If something is not getting correctly extracted,[file a bug on their repo](https://github.com/microsoft/Recognizers-Text), go to issues, click on new issue, describe the bug with guidelines provided, showing an example of expected behavior

* If the bug is valid, it will be in one of the upcoming releases of the text-recognizer, which will soon reflect in LUIS

### Things to Note

* Note that you can add and refine your prebuilt entity with your own data by creating a machine learned entity and use the prebuilt entity as a feature to it. That way all the additional labels from your data will learn the context of where the prebuilt entity exist in your application.
