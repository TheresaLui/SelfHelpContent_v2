<properties
pageTitle="manage-luis-apps-and-migrations"
description="Understanding and troubleshooting for migrations"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683913"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_ManageLUISApps_ManageAuthorsAndCollaborators"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Manage Authors and Collaborators
## **Recommended Steps**

* A LUIS application owner may add users to his/her apps and they have the control to build, train, and publish the app

* Term given to identify these users and how to manage them differs and depends on the current status of your account

* **Two possible states of your account:** [Migrated](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#what-is-migration) or not migrated

* If owner's application is **not migrated**, users added to the owner applications are called **Collaborators** and they are added on the application level. They will have visibility and control on only the applications that the owner chooses.

* If owner's application is **migrated**, users added to the owner applications are called **Contributors** and they are added on the resource level. They will have visibility and control over all applications the owner owns.

### **Migration**

* Learn more about [the migration process](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#note-before-you-migrate) and how if effects owners and collaborators on an application

* Migration will be will be enforced by August 30th, 2020

* Make sure that your account is associated with a valid Azure subscription to be able to Migrate. If you do not have an Azure subscription, create a [free trial](https://azure.microsoft.com/free/).

* To Migrate, you need to create a new authoring resource, **make sure it is an authoring and not a runtime/prediction LUIS resource**, either from the [LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#migration-steps) or from the [Azure portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal)

* If you are the owner or administrator of your Azure subscription, you can [add a contributor to the authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-collaborate#add-contributor-to-azure-authoring-resource) to collaborate on the same applications

* Learn about the [permissions needed to add contributors to your resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#add-contributors-to-authoring-resources)

* There is a limit to the number of authoring keys created per subscription per region. This limit is **10 resources per subscription per region**

* If an application is in production and collaborators have prediction resources assigned to the app, migration will be blocked for both owner and collaborator. Please read [the recommended steps to successfully migrate](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#prediction-resources-blocking-migration)

* [Troubleshooting if migration fails](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#troubleshooting-migration-process)
