<properties
pageTitle="Authentication failures"
description="Authentication failures"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683888"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_APIsErrorsAndExceptions_authenticationFailures"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Authentication Failures
## **Recommended Steps**

### If access is denied while accessing the LUIS endpoint

* Ensure that the key you are using to call LUIS APIs is assigned to the LUIS application being called. Sign-in to the [appropriate LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions) that you are creating your applications in and navigate to the [prediction under Azure resources under the manage tab in the top bar](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app).
* If the key is not assigned, click on [assign prediction resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app) and select the appropriate LUIS key
* Ensure that the key you are using is in your code is not an invalid, malformed, or empty key
* Ensure that the [key matches the region the application is published in](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-regions-are-tied-to-authoring-regions). Otherwise this could cause the error.

### If your access is denied while using LUIS Authoring APIs

* Ensure that the key you are using is in fact an authoring or a starter key and not a prediction runtime key
* Ensure that the key you are using is in fact an authoring or a starter key and not a prediction runtime key
* Ensure that they key you are using is assigned to the application you are calling. Sign-in to the [appropriate LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions) you have been authoring your apps in and navigate to [authoring under Azure resources under the manage tab in the top bar](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app).
* If you have validated that your keys are the correct ones, make sure that you have been [given consent to your application by your Azure Active Directory Tenant admin](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-collaborate#azure-active-directory-tenant-user)
* Validate first that you are an owner or collaborator or contributor of the LUIS app you are trying to access
* If not, you will not be able to see the application and will not have access to modify it. Request from the app owner to [add you as a contributor or collaborator](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-collaborate) depending whether you are a [migrated or a non migrated user](https://docs.microsoft.com//azure/cognitive-services/luis/luis-migration-authoring).
* Check that you are [assigning an Ocp-Apim-Subscription-Key to your request header](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-query-prediction-runtime-resource-without-using-luis-portal). The Ocp-Apim-Subscription-Key is your authoring/programmatic key.
* Ensure that the [key location matches the authoring region of your application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions), or this could cause the error

## **Recommended Documents**

* Learn more on [common API response codes](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-response-codes)
* [Understand the differences between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-keys)
* Learn more about [LUIS authoring and publishing regions along with their associated keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions)
* Learn how to [purchase a LUIS paid tier (S0) runtime key](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#change-pricing-tier) and [assign it to your application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app)
