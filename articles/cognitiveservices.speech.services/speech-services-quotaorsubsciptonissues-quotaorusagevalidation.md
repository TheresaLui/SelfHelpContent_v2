<properties
pageTitle="Quota or usage validation"
description="Quota or usage validation"
service="microsoft.CognitiveServices"
resource="accounts"
authors="alexeyo26"
ms.author="alexeyo"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683856"
productPesIds="16870"
cloudEnvironments="public, MoonCake, fairfax"
articleId="Speech_Services_quotaOrSubsciptonIssues_quotaOrUsageValidation"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Quota or usage validation

See all existing Speech Services quotas and limits:

- Speech-to-text
- Text-to-speech

## Validation of Concurrent Request limit

Existing value of Concurrent Request limit parameter for **Standard (S0)** price tier is **not** visible via Azure portal, Command-Line tools, or API requests. To verify the existing value, proceed further and create an Azure Support Request.

Please, have the following information ready and enter it to the *Description* field of the *Details* part of this support request:

- Information for Speech-to-text
- Information for Text-to-speech  

## **Recommended Documents**

!!!




If you receive many **Response Codes 429 ("Too many requests")** or you anticipate a serious growth of the workload review your Speech resource quotas and limits. Request adjustment if needed and possible and follow described best practices.

Jump to [**Text-to-speech: Recommended Steps**](#text-to-speech-recommended-steps)

## **Speech-to-text: Recommended Steps**

- Get familiar with !!!
  - Ensure you follow !!!
- If applicable request the increase

## **Text-to-speech: Recommended Steps**

- Get familiar with !!!
  - Ensure you follow !!!
- If applicable request the increase

## **Recommended Documents**

!!!






* If you exceed your transactions-per-second (TPS) quota, you receive an **HTTP 429 error**. If you exceed your transaction-per-month (TPS) quota, you receive **an HTTP 403 error**.

* When creating a LUIS account, a starter key is automatically generated for the account for a non-migrated users.

* A new users will require to associate their LUIS application with a [F0 authoring resource key](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal).

* The **F0 authoring key** and the **starter key** allow up to 1 million calls to LUIS authoring/programmatic APIs a month and allow up to 1000 endpoint calls a month.

* Associate your LUIS applications with the [F0 prediction key](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app) to allow up to 10,000 endpoint calls a month.  

## **Recommended Steps**

* If you are getting a **403 quota exceeded response** and using a key, you have exceeded the F0 authoring quota or the F0 prediction quota and it will be replenished at the beginning of next month.  

* Use Azure portal to check [how many transactions a key has made](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#viewing-azure-resource-metrics).

* To exceed the endpoint calls per month, [purchase a LUIS paid tier (S0) runtime key through Azure](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#change-pricing-tier) and [assign it to your application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app).

* Learn about [LUIS Pricing details and the transaction per second(TPS) for each key](https://azure.microsoft.com/pricing/details/cognitive-services/language-understanding-intelligent-services/).

* Learn about [LUIS resource boundaries and key tiers](https://docs.microsoft.com/azure/cognitive-services/luis/luis-boundaries#key-limits).

* Learn about [LUIS Key management experience](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-keys) and the differences between authoring and prediction keys.

* If your application needs more than the defined intents and entities, consider using [Dispatch tool](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-enterprise#dispatch-tool-and-model). It is a CLI tool which allows you to have a parent app that dispatches between multiple child LUIS apps.

* Another option to work around the transaction per second limit is to use [LUIS on containers](https://docs.microsoft.com/azure/cognitive-services/luis/luis-container-howto?tabs=v3). Containers give you the freedom to manage your LUIS application in a connected container environment.
