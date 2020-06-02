<properties
pageTitle="Manage LUIS Apps and Migrations"
description="Understanding and troubleshooting for migrations"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683912"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax"
articleId="LUIS_Conversation_ManageLUISApps_ManageAuthoringKeys"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Manage Authoring Keys

## **Getting started**

* To link Azure Authoring keys or resources on your application, you must first [Migrate](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-migration-authoring).
* **Migration** is the process of changing authoring authentication from an email account to an Azure resource.
* Applications can be shared with others on the resource and subscription level after migration. These are called collaborators.
* While not currently required, switching to an Azure resource will be enforced by August 30th, 2020.
* To Migrate, you need to first create a new authoring resource, **make sure it is an authoring and not a runtime/prediction LUIS resource**, either from the LUIS portal or from the Azure portal.


## **How to create an authoring resource from the Azure Portal?**

* You must first ensure that your account is associated with a valid Azure subscription. If you do not have an Azure subscription, create a free one. Noting that having an Azure subscription is a prerequisite to create any Azure resources.
* When landing on the Azure portal, search for Language Understanding and click on create a new resource. Choose the Authoring Tab from above and fill in the template as in [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal).

    **Note:** You need to choose the authoring region based on which authoring portal you will build and create your application in. Please check [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions) 3 LUIS authoring regions and their portals.

* To share and collaborate and the same applications, you can add **contributors** to your authoring resource and they would have access to all apps under this resource. This can be managed from the Azure portal by opening the authoring resource and using the Access control (IAM) page. Add a user with their email address and the contributor role. Please read documentation [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-collaborate) for details on how to add contributors to your resource.

## **How to create an authoring resource from the LUIS Portal?**

You can create an authoring resource from the LUIS portal while migrating or after migration.

* **While Migrating:** Please follow steps [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-migration-authoring-steps#access-the-migration-process) on how to create a new Authoring resource while migrating.
* **After Migration:** In the upper tool bar, if you click on the user settings, you can create a new authoring resource by clicking on the button. Make sure that you have a valid subscription and an azure resource name.


## **Troubleshooting**

* Ensure that you are associated with an Azure Subscription before creating a new authoring resource. If you don't, create one from the Azure Portal.
* Ensure that you have an Azure Resource group in the same region you are signed in on before creating a new authoring resource. If you don't, create one from the Azure portal.
* Ensure that your subscription has <10 authoring resources before creating a new one. If your subscription has **10 or more Authoring resources**, you wont be able to create a new authoring key.
* If you are added as a contributor to a resource but can not find
