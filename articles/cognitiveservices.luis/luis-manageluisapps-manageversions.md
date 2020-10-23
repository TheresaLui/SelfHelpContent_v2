<properties
pageTitle="manage-versions"
description="Understanding how to work and manage versions"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683915"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_ManageLUISApps_ManageVersions"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Manage Versions or Export and Import
## **Recommended Steps**

### **Getting started**

* Versions are copies of your active model, that allows you to build, edit and test different models without impacting staging or production applications

* It allows you to compare and contrast between different stages of an application

* It is a good practice to [create a new version](https://docs.microsoft.com/azure/cognitive-services/LUIS/luis-concept-app-iteration#create-a-new-version-for-each-cycle) before making changes to the active model

* **To work with versions**, open your app by selecting its name on My Apps page, and then select Manage in the top bar, then select Versions in the left navigation. The list of versions shows which versions are published, where they are published, and which version is currently active.

* You can [clone](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-manage-versions#clone-a-version), [Set active version](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-manage-versions#set-active-version)), [import](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-manage-versions#import-version) and export versions

* When exporting, choose "JSON" to export for backup and choose **Export for container** to use this app in a [LUIS container](https://docs.microsoft.com/azure/cognitive-services/luis/luis-container-howto?tabs=v3)

* [Manage contributor changes with versions](https://docs.microsoft.com/azure/cognitive-services/LUIS/luis-concept-app-iteration#manage-contributor-changes-with-versions-and-contributors)

### **Troubleshoot Version Errors**

* If you get a **tokenizer error** when importing, then you are trying to import a version that uses a different tokenizer than the app currently uses. To fix this, [Migrating between tokenizer versions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-language-support#migrating-between-tokenizer-versions).

* [Read more about tokenization](https://docs.microsoft.com/azure/cognitive-services/luis/luis-language-support#tokenization) and [custom tokenization versions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-language-support#custom-tokenizer-versions)

* If you find other errors, please open an ICM Ticket.
