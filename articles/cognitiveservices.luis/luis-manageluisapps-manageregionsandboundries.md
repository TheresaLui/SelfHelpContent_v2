<properties
pageTitle="Manage-regions-and-boundaries"
description="Understanding and Managing Regions"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683917"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_ManageLUISApps_ManageRegionsAndBoundaries"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Manage Regions and Boundaries
## **Recommended Steps**

LUIS has 3 authoring regions that are supported by 3 corresponding LUIS portals. Every application in every authoring region has a set of regions you can publish to. To publish a LUIS app to more than one region, you need at least one key per region.

### Getting started

* **Authoring regions** is where you build, train, test and manage your application. [LUIS has 3 authoring regions (US, Europe, Australia) and for each region a corresponding portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions).

* Create an **authoring resource** from the [LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#migration-steps) or from the [Azure portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal) to author applications. **Location of authoring resource must be the same as the authoring portal region** you will be using.

* **Publishing regions** is where you [publish your application and make it available for your client applications to hit its endpoint](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-publish-app) after you have finalized the app building process .

* Create a **prediction/runtime resource** from [Azure Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-resources-in-the-azure-portal) and [assign it to your application in the LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app).

* The app is published to all regions associated with the LUIS resources added in the LUIS portal. However, [Publishing regions are tied to authoring regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-regions-are-tied-to-authoring-regions)

* If your app is currently in the wrong authoring region, export the app, and import it into the correct authoring region for your publishing region.

* If you are authoring in the **US (luis.ai) portal**, here are the [all publishing regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-to-other-regions) associated with it.

* If you are authoring in **Europe portal (eu.luis.ai)**, here are the [European publishing regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-to-europe) associated with it.

* If you are authoring in **Australia portal (au.luis.ai)**, here are the [Australian publishing regions](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#publishing-to-australia) associated with it.

* [A public app](https://docs.microsoft.com/azure/cognitive-services/luis/luis-concept-keys#access-for-private-and-public-apps) is published in all regions so that any valid prediction resource can call it.
