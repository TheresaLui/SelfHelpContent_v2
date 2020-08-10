<properties
pageTitle="manage-luis-apps-and-migrations"
description="Understanding and troubleshooting for migrations"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683912"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_ManageLUISApps_ManageAuthoringKeys"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Manage Authoring Keys

## **Recommended Steps**

* To link Azure Authoring keys or resources on your application, you must first [Migrate your account](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#what-is-migration)

* To Migrate, you need to create a new authoring resource. **Make sure it is an authoring and not a runtime/prediction LUIS resource**, either from the [LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#migration-steps) or from the [Azure portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal

* Create [authoring resources in Azure CLI](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-resources-in-azure-cli)

* Make sure that your account is associated with a valid Azure subscription to be able to create any Azure resource. If you do not have an Azure subscription, create a [free trial](https://azure.microsoft.com/free/)

* You need to choose the authoring region based on which authoring portal you will build and create your applications in. Please check the [3 LUIS authoring regions and their portals](https://docs.microsoft.com/azure/cognitive-services/luis/luis-reference-regions#luis-authoring-regions).

* If you are the owner or administrator of your Azure subscription, you can [add a contributor to the authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-collaborate#add-contributor-to-azure-authoring-resource) to collaborate on the same applications

* Learn about the [permissions needed to add contributors to your resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#add-contributors-to-authoring-resources)

* There is a limit to the number of authoring keys created per subscription per region. This limit is **10 resources per subscription per region**.

* There is a **restriction in the naming conventions for authoring resources**. Names can only include alphanumeric characters and the '-' character; it must be between 2 and 64 characters in length and cannot end with a '-'.

* [Assign a new authoring resource to your application](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#assign-a-resource-to-an-app)

* [Un-assign your authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#unassign-resource)

* [Reset your authoring key](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#reset-authoring-key) if it is compromised

* Learn the [difference between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription)
