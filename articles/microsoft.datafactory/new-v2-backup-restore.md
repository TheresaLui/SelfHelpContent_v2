<properties
	pageTitle="Data Factory V2 - Backup and Restore"
	description="How to keep a backup or restore a deleted data factory resource"
	infoBubbleText=""
	authors="hecepeda"
	ms.author="hecepeda"
	articleId="new-v2-backup-restore.md"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32781329"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Factory Backup and Restore

## **Recommended Steps**

### **Restore**

Azure Data Factory does not retain any customer data after factory deletion has been requested. **If a factory has been deleted, there is no way to restore the resource.** If the factory was integrated with a Git repository, the factory can be re-created from the ARM Template in the publish branch or from the existing resources in the repository. We highly recommend Git integration as backup for accidental deletion.

To recover a Deleted Data Factory that had Source Control enabled, use the following steps:

1. Create a new Azure Data Factory
2. Configure Git with the same settings, but make sure **Import existing Data Factory resources to repository** is selected and for the _Branch to import resources into_, choose **Create New**
3. Create a pull request to merge the changes to the collaboration branch
4. Publish

**Note:** If you had a Self-hosted Integration Runtime in the deleted ADF, you will need to create a new instance in the new ADF. Make sure you uninstall and reinstall the Self-Hosted IR software on the instance that you were using so that a new key is obtained.

After the setup of the Self-Hosted IR is completed, you will need to change the Linked Service to point to the new IR and test the connection, or it will fail with error "Invalid reference."

### **Backup**

Azure Data Factory provides Source Control integration with Git repositories to manage version control and history of changes. To review the benefits of Source Control integration, and a step by step guide on how to configure it, review [Advantages of Git integration](https://docs.microsoft.com/azure/data-factory/source-control#advantages-of-git-integration).

After Source Control integration is defined, you can implement continuous integration and delivery by following the documentation about [Continuous integration and delivery in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment).

 
