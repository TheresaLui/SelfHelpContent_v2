<properties
pageTitle="With Bing Spell Check"
description="With Bing Spell Check"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683952"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_integratingLUISWithOtherServices_withBingSpellCheckV7"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# With Bing Spell Check v7

### Getting Started

* LUIS offers spell checking through [Bing Spell Check v7](https://azure.microsoft.com/services/cognitive-services/spell-check/) to correct misspelled words in utterances before LUIS predicts the score and entities of the utterance

* Note that this **feature is not supported in the V3 API** for prediction endpoints

* Before publishing your LUIS application, [change publish settings with Bing spell check as on](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-publish-app#publishing) in your settings

* You must [create a Bing Spell Check resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-tutorial-bing-spellcheck#create-endpoint-key) in the Azure portal independently from LUIS

* Include the [Bing Spell Check key parameter to the LUIS endpoint URL](https://docs.microsoft.com/azure/cognitive-services/luis/luis-tutorial-bing-spellcheck#adding-the-key-to-the-endpoint-url) when using the [published LUIS endpoint](https://docs.microsoft.com/azure/cognitive-services/luis/luis-get-started-get-intent-from-browser?tabs=V3-1-1%2CV3-2-1%2CV3-3-1)


## **Recommended Steps**

* Learn more on how to [send misspelled utterances](https://docs.microsoft.com/azure/cognitive-services/luis/luis-tutorial-bing-spellcheck#send-misspelled-utterance-to-luis) or [ignoring spelling mistakes](https://docs.microsoft.com/azure/cognitive-services/luis/luis-tutorial-bing-spellcheck#ignore-spelling-mistakes) with Bing Spell Check.

* If you feel there is something that is getting incorrectly spell-checked, you first need to identify whether the issue is from LUIS or Bing Spell Check's side

* Use the same utterance and call Bing Spell Check v7 API independently first

* If it is getting incorrectly spell-checked, open an issue on Bing Spell Check v7. If it is fixed in Bing Spell Check v7, but is getting incorrectly returned in LUIS, open an issue on LUIS.
