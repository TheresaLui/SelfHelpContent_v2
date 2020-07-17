<properties
pageTitle="Customer Managed Keys"
description="Customer Managed Keys"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32742799"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_ManageLUISApps_customerManagedKeys"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Customer Managed Keys

* By default, your subscription uses Microsoft-managed encryption keys. There is also an option to manage your subscription with your own keys with Customer managed keys.

* [Customer-managed keys (CMK)](https://docs.microsoft.com/azure/cognitive-services/luis/luis-encryption-of-data-at-rest#customer-managed-keys-with-azure-key-vault), also known as Bring your own key (BYOK), offer greater flexibility to create, rotate, disable, and revoke access controls.

* You must use [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview) to store your customer-managed keys.

* Since CMK is still in private preview, to request the ability to use customer-managed keys, [fill out and submit this form](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR3k4-f_9d9xPhWkgOUub9YhUNDZJUERRVVVDME4xNDVNRjEwMTNZV1dHSS4u).

* Please check the limitations](https://docs.microsoft.com/azure/cognitive-services/luis/luis-encryption-of-data-at-rest#limitations) when using CMK with LUIS.  

## **Recommended Documents**

* Learn more about [Cognitive Services encryption](https://docs.microsoft.com/azure/cognitive-services/luis/luis-encryption-of-data-at-rest#about-cognitive-services-encryption).

* Learn more about [Customer-managed keys for LUIS](https://docs.microsoft.com/azure/cognitive-services/luis/luis-encryption-of-data-at-rest#customer-managed-keys-for-language-understanding).
