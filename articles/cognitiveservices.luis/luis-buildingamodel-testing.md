  <properties
	pageTitle="Testing"
	description="Testing"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683938"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="LUIS_Conversation_buildingAModel_Testing"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Testing
## **Recommended Steps**

* Training and testing an app is an **iterative process**. After you train your LUIS app, testing allows you to try out your trained app and verify its results by checking if the intents and entities are recognized correctly. If they're not, make updates to the LUIS app, then train, and test again.

* The [interactive testing pane](https://docs.microsoft.com/azure/cognitive-services/luis/luis-interactive-test) allows you to input a test utterance and returns the intent and entities extracted from it

* Scoring in testing is a [prediction score](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-prediction-score) that indicates the degree of confidence LUIS has for results of a user utterance

* [Batch testing](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-batch-test) allows you to upload batches of 1000 labelled utterances and returns results for the actual predictions against your labels

* It is best if you test your application against utterances that are not included in the training data to better verify the performance of your application

* Testing is currently only available through the LUIS portal. The batch testing API is scheduled to be released before end of 2020.

* Use [LUIS authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to be able to test from the LUIS portal
