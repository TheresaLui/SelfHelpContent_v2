<properties
pageTitle="Regional Portal Issues"
description="Regional portal issues"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683933"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_LuisPortal_regionalPortalIssues"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Regional Portal Issues

LUIS has 3 authoring regions that are supported by 3 corresponding LUIS portals. Every application in every authoring region has a set of regions you can publish to. To publish a LUIS app to more than one region, you need at least one key per region.

## **Recommended Steps**

* **Authoring regions** is where you build, train, test and manage your application. [LUIS has 3 authoring regions (US, Europe, Australia) and for each region a corresponding portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions)

* Create an **authoring resource** from the [LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#migration-steps) or from the [Azure portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to author applications. **Location of authoring resource must be the same as the authoring portal region** you will be using

* **Publishing regions** is where you [publish your application and make it available for your client applications to hit its endpoint](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-publish-app) after you have finalized the app building process

* Create a **prediction/runtime resource** from [Azure Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-resources-in-the-azure-portal) and [assign it to your application in the LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app)

* Understand the [difference between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription)

* The app is published to all regions associated with the LUIS resources added in the LUIS portal. However, [Publishing regions are tied to authoring regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-regions-are-tied-to-authoring-regions)

* If your app is currently in the wrong authoring region, export the app, and import it into the correct authoring region for your publishing region

* If you are authoring in the **US (luis.ai) portal**, here are the [all publishing regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-to-other-regions) associated with it

* If you are authoring in **Europe portal (eu.luis.ai)**, here are the [European publishing regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-to-europe) associated with it

* If you are authoring in **Australia portal (au.luis.ai)**, here are the [Australian publishing regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-to-australia) associated with it

* [A public app](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-keys#access-for-private-and-public-apps) is published in all regions so that any valid prediction resource can call it

* If **you can not login to LUIS**, it may be because the admin of the subscription hasn’t given access to you or to the company to use LUIS. You will need to contact the admin and make them [add LUIS to the list of approved services they can use](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-collaborate#azure-active-directory-tenant-user).
