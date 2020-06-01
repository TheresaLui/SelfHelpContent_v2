<properties
pageTitle="Manage Versions"
description="Understanding how to work and manage versions"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683915"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax"
articleId="LUIS_Conversation_ManageLUISApps_ManageVersions"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Manage Versions or Export and Import

## **Getting started**

* **What are versions?** Versions are copies of your model, that allows you to build, edit and test different models without impacting staging or production applications. LUIS allows you to have multiple versions per application.
* **Are they required for me to do?** No, it just allows you to compare and contrast between different stages of an application. It is a good practice to clone the current active model to a different version of the app before making changes to the model.
* **What is meant by an active version?** The active version is the version you are editing in the LUIS portal Build section with intents, entities, features, and patterns. When using the authoring APIs, you don't need to set the active version because the version-specific REST API calls include the version in the route.
* **How do I work with versions?** To work with versions, open your app by selecting its name on My Apps page, and then select Manage in the top bar, then select Versions in the left navigation. The list of versions shows which versions are published, where they are published, and which version is currently active.
* **What actions I can do with versions?** You can [clone](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-manage-versions#clone-a-version), activate a version (setting it to be the active version), [import](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-manage-versions#import-version) and export versions. When exporting, choose "JSON" to export for backup and choose **Export for container** to use this app in a [LUIS container](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-container-howto?tabs=v3).



## **Troubleshoot Version Errors**

* If you get a **tokenizer error** when importing, then you are trying to import a version that uses a different tokenizer than the app currently uses. To fix this, import the file as a new app, instead of a version as there is currently no support for version-level tokenization and tokenization only happens at app level. This action means the new app has a different app ID but uses the tokenizer version specified in the file.
* If you find other errors, please open an ICM Ticket.
