<properties
pageTitle="Manage Regions and Boundaries"
description="Understanding and Managing Regions"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683917"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax"
articleId="LUIS_Conversation_ManageLUISApps_ManageRegionsAndBoundaries"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Manage Regions and Boundaries

LUIS has 3 authoring regions that are supported by 3 corresponding LUIS portals. Every application in every authoring region has a set of regions you can publish to. To publish a LUIS app to more than one region, you need at least one key per region.

## Getting started

* **What are authoring regions?** Regions where you can build, train, test and manage your application. LUIS has 3 authoring regions (US, Europe, Australia) and for each region a corresponding portal. Check [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions) the corresponding LUIS portal for each region along with the Azure region name.  
* **What are publishing regions?** When you finish building, training, and testing your active LUIS app, you make it available to your client application by [publishing it to the endpoint](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-publish-app). The app is published to all regions associated with the LUIS prediction endpoint resources added in the LUIS portal from the [manage page in your application](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app).

**NOTE:** The authoring region app can only be published to a corresponding publish region. If your app is currently in the wrong authoring region, export the app, and import it into the correct authoring region for your publishing region. For example, LUIS apps created in the US portal, it can be published to all endpoints except the European and Australian regions. Please find more details in the documentation about [Europe publishing regions](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-reference-regions#publishing-to-europe), [Australia publishing regions](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-reference-regions#publishing-to-australia), and [Publishing to any other regions](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-reference-regions#publishing-to-other-regions) supported by LUIS.


 * **Can I publish my app to all regions at once?** Yes, A public app is published in all regions so that a user with a region-based LUIS resource key can access the app in whichever region is associated with their resource key. You need to manage your authoring process and the resulting trained model in all 3 authoring regions.
* **Do I need to create authoring resources in the same region as the authoring region?**
* **What Happens if I created an authoring resource from Azure portal in a different region than the portal I am currently using?**

## Authoring Resources
* **From where can I create an Authoring resource?** Authoring resources can be either created from the Azure portal or the LUIS portal.
* **How can I create an Authoring resource from Azure?** Go to [Azure Portal](https://portal.azure.com/) and ensure that you are associated with a valid Azure subscription. If you do not have an Azure subscription, create a free one. Noting that having an Azure subscription is a prerequisite to create any Azure resources. Search for Language Understanding and click on create a new resource. Choose the Authoring Tab from above and fill in the template as in [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal).
    **Note:** You need to choose the authoring region based on which authoring portal you will create your model in. If you are planning to create and publish your application in the Europe region, you need to create the resource in the Europe region.  
* **How can I create an Authoring resource from LUIS?**
      * If you are [Migrated](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-migration-authoring), then you already have an authoring resource that is linked to your application. You can always create a new one from the LUIS portal [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app).
      * If you are not migrated yet, you can create an authoring resource while migrating. You can find the steps [here]. Noting that the authoring resource that will be created in the same region as in the same current portal the user is on. For example, if you are on the luis.ai portal, the authoring resource that will be created will be in West US region.  

## Prediction/runtime Resources
* **From where can I create a prediction/runtime resource?** Prediction/runtime resources can be either created from the Azure portal or the LUIS portal.
* **How can I create a Prediction/runtime resource from Azure?** Go to [Azure Portal](https://portal.azure.com/) and ensure that you have a valid Azure subscription. If you do not have an Azure subscription, create a free one. Noting that having an Azure subscription is a prerequisite to create any Azure resources. Search for Language Understanding and click on create a new resource. Choose the prediction tab from above and fill in the template.
* **How can I create a Prediction/runtime resource from LUIS?** From your application in the manage tab, click on Azure Resources menu on the left and follow the steps [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app) to add a new prediction resource to your app.


## Troubleshoot

* **If I do not see the Authoring resource I created in the LUIS portal?**
Then you may have created the authoring resource in a different region than the authoring portal you are currently on. Go to the azure portal and check the region of the resource that you have created. If it is not the same as the authoring region portal you are using, create a new one in the proper region.  

* **If I created my application in an Authoring region that does not support the region that I wish my application to be published in?**
You can export your application and import back to the authoring region portal where you would like your applications to be published in.
