<properties
pageTitle="Migrations and Troubleshooting"
description="Migrations and Troubleshooting"
service="microsoft.CognitiveServices"
resource="accounts"
authors="SaraKandil"
ms.author="a-sakand"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683914"
productPesIds="16869"
cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
articleId="LUIS_Conversation_LuisPortal_manageUserAndRoles"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Migrations and Troubleshooting

* **Two possible states of your account:** [Migrated](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#what-is-migration) or not migrated

* Migration in LUIS is simply linking your account to an LUIS Azure resource

* Migration will be mandatory for any LUIS user

## **Recommended Steps**
* Learn more about [the migration process](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#note-before-you-migrate) and how it effects owners and collaborators on an application

* Make sure that your account is associated with a valid Azure subscription to be able to Migrate. If you do not have an Azure subscription, create a [free trial](https://azure.microsoft.com/free/).

* To Migrate, you need to create a new authoring resource, **make sure it is an authoring and not a runtime/prediction LUIS resource**, either from the [LUIS Portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#migration-steps) or from the [Azure portal](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription#create-luis-resources-in-azure-portal)

* If you are the owner or administrator of your Azure subscription, you can [add a contributor to the authoring resource](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-collaborate#add-contributor-to-azure-authoring-resource) to collaborate on the same applications

* There is a limit to the number of authoring keys created per subscription per region. This limit is **10 resources per subscription per region**. You will get an error of "Failed retrieving user's Azure information, retry again later."

* If an application is in production and collaborators have prediction resources assigned to the app, **migration will be blocked for both owner and collaborator**. Please read [the recommended steps to successfully migrate](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#prediction-resources-blocking-migration).

* Please check [troubleshooting guides](https://docs.microsoft.com/azure/cognitive-services/luis/luis-migration-authoring#troubleshooting-migration-process) if migration is failing

* Learn the [difference between authoring and prediction keys](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-azure-subscription)

* If **you can not login to LUIS**, it may be because the admin of the subscription hasn’t given access to you or to the company to use LUIS. You will need to contact the admin and make them [add LUIS to the list of approved services they can use](https://docs.microsoft.com/azure/cognitive-services/luis/luis-how-to-collaborate#azure-active-directory-tenant-user).
