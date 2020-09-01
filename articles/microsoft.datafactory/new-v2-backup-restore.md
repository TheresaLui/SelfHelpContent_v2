<properties
	pageTitle="Data Factory V2 - Backup and Restore"
	description="How to keep a backup or restore a deleted data factory resource"
	infoBubbleText=""
	authors="hecepeda"
	ms.author="hecepeda"
	articleId="new-v2-backup-restore.md"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32742803"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Factory Backup and Restore

## **Recommended Steps**

### **Restore**

Azure Data Factory does not retain any customer data after factory deletion has been requested. **If a factory has been deleted, there is no way to restore the resource.** If the factory was integrated with a Git repository, the factory can be recreated from the ARM Template in the publish branch or from the existing resources in the repository. Git integration is highly recommended as backup for accidental deletion.

### **Backup**

Azure Data Factory provides Source Control integration with Git repositories to manage version control and history of changes. To review the benefits of Source Control integration, and a step by step guide on how to configure it, please review [Advantages of git integration](https://docs.microsoft.com/azure/data-factory/source-control#advantages-of-git-integration).

Once Source Control integration is defined you can implement continuous integration and delivery by following the documentation on [Continuous integration and delivery in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment).

 
