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

## **Recommended Documents**

### Getting started

* A LUIS application owner may add users to his/her apps and they have the control to build, train, and publish the app.
* Term given to identify these users and how to manage them differs and depends on the current status of the app.
* **Two possible states of your apps:** [Migrated](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-migration-authoring) or not migrated.
* If owner's application is **not migrated**, users added to the owner applications are called **Collaborators** and they are added on the application level. i.e.: they will have visibility and control on only the applications that the owner chooses.
* If owner's application is **migrated**, users added to the owner applications are called **Contributors** and they are added on the resource level. i.e.: they will have visibility and control over all applications the owner owns.

### Migration

* **What is Migration?** Migration is the process of changing authoring authentication from an email account to an Azure resource.
* **Is Migration required?** While not currently required, switching to an Azure resource will be enforced by August 30th, 2020.
* **Are there any prerequisites for migration?** Yes, You need to be associated with a valid Azure Subscription.
* **How to Migrate?** Create a new authoring resource, **make sure it is an authoring and not a runtime LUIS resource**, either from the LUIS portal or from the Azure portal. If you have an existing authoring resource on your subscription, you can migrate to it as well from the LUIS portal. Please read documentation [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-migration-authoring-steps) for detailed steps on how to migrate.
* **How to add contributors to my resource?** This can be managed from the Azure portal by opening the authoring resource and using the Access control (IAM) page. Add a user with their email address and the contributor role. Please read documentation [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-collaborate) for details on how to add contributors to your resource.
* **What do I do if Migration failed?** Check the below troubleshoot section.
* **Will my applications migrate with me?** Yes, if you are the owner of the application, all your applications will migrate and will be automatically associated with the authoring resource you migrated on.
* **If I am not an owner to an application, can I migrate?** Yes, any LUIS user can and will eventually need to migrate. However, applications that are not owned by you will not migrate with you. You will need to export the applications you need and import it back after migration.


**If owner migrates, what happens to collaborators?**

* Owners will be prompted to send emails to inform their collaborators before migrating. They may choose to send emails or not.
* Applications will migrate with owners and will disappear from collaborator side.
* If collaborator wants to access the application, they will need to first migrate.
* After migration, owner of application must add user as a contributor on the Azure resource from the Azure portal through the Access control (IAM) page. They shall add the email address and the contributor role for the user as described [here](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-collaborate).
* Contributors will now be able to see the applications under the authoring resource that they have now access on.

**If collaborator migrates, what happens to owners?**

* Nothing will happen to the owner if collaborators migrate and they won't know that their Collaborators have migrated.
* They will continue to use their applications normally.

**PLEASE NOTE:** If any collaborator owns a **Runtime Resource** and associates it with the owner's application, migration will fail for both the owner and collaborator. Collaborator will need to either remove the runtime resource from the application or give access to owner from Azure portal for the migration to be successful.


### Troubleshoot Migration Errors

* Ensure that you are associated with an Azure Subscription before creating a new authoring resource. If you don't, create one from the Azure Portal.
* Ensure that you have an Azure Resource group in the same region you are signed in on before creating a new authoring resource. If you don't, create one from the Azure portal.
* Ensure that your subscription has <10 authoring resources before creating a new one. If your subscription has 10 or more Authoring resources, migrate to an existing authoring key instead of creating a new one.
* If your have a collaborator and they assigned prediction resources to your applications, make sure to first inform them of the migration, then remove them as collaborators from the application.
* If you are collaborating on an application an you are failing to migrate, make sure that you remove any prediction resources you have assigned to these applications. Also make sure to export your application before migrating.
