  <properties
	pageTitle="How to Build a Model using intents in LUIS"
	description="How to Build a Model using intents in LUIS"
	service="microsoft.CognitiveServices"
	resource="accounts"
	authors="SaraKandil"
	ms.author="a-sakand"	
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32683907"
	productPesIds="16869"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec" 
	articleId="LUIS_Conversation_BuildModel_Intents"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# How to Build a Model using intents in LUIS
Intents in LUIS allow you to identify the intent or objective of a sentence. Train Intents by adding example utterances to an Intent. For example, a "Cancel" intent would include examples such as: 

* I would like to cancel my subscription
* Please cancel that action
* Stop the current action
  	  
Intents are best used when mapped to different actions or ideas. Using the same example, it would not be a good idea of having 2 intents, one for "Cancel Subscription" and another for "Cancel Payment" because they would typically have a lot of the same keywords. It is also important to use a variation of ways to express a certain intent when adding examples to help LUIS generalize better. To better resolve more details in the intent, use entities to capture things like "what" you are cancelling.

Intents are mutually exclusive, which means their scores are on a scale of 0 to 1 independently of each other. 2 LUIS intents can have high scores for the same utterance if they use a lot of the same vocabulary. 

If a specific utterance is not getting matched as the expected top intent, then you can use the Analytics Dashboard to obtain actionable advice on weak intents. It is likely that there is another intent that contains utterances with several of the same words of the utterance getting incorrectly detected. The Analytics Dashboard will help identify which intents are conflicting.

## **Recommended Documents**

* [Learn more about Intents here](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-intent)
