<properties
  pagetitle="Azure Data Factory Backup and Restore&#xD;"
  description="How to keep a backup or restore a deleted data factory resource"
  ms.author="hecepeda,haoc"
  selfhelptype="Generic"
  supporttopicids="32781329"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="new-v2-backup-restore.md"
  ownershipid="AzureData_DataFactory" />
# Azure Data Factory Backup and Restore

## **Recommended Steps**

### **Restore**

Azure Data Factory does not retain any customer data after factory deletion has been requested. **If a factory has been deleted, there is no way to restore the resource.** If the factory was integrated with a Git repository, the factory can be re-created from the ARM Template in the publish branch or from the existing resources in the repository. We highly recommend Git integration as backup for accidental deletion.

To recover a Deleted Data Factory that had Source Control enabled, use the following steps:

1. Create a new Azure Data Factory
2. Configure Git with the same settings, but make sure to select **Import existing Data Factory resources to repository**. For the **Branch to import resources into**, choose **Create New**.
3. Create a pull request to merge the changes to the collaboration branch
4. Publish

**Note:** If you had a Self-hosted Integration Runtime in the deleted ADF, you will need to create a new instance in the new ADF. Make sure you uninstall and reinstall the Self-Hosted IR software on the instance that you were using so that a new key is obtained.

After the setup of the Self-Hosted IR is completed, you will need to change the Linked Service to point to the new IR and test the connection, or it will fail with error "Invalid reference."

### **Backup**

You can back up your data factory if the factory is integrated with a Git repository. The factory can be recreated from the ARM Template in the publish branch or from the existing resources in the repository. Git integration is highly recommended as backup for accidental deletion. Azure Data Factory allows you to configure a Git repository with either Azure Repos or GitHub. Git is a version control system that allows for easier change tracking and collaboration. To review the benefits of Source Control integration, and a step by step guide on how to configure it, review [Advantages of Git integration](https://docs.microsoft.com/azure/data-factory/source-control#advantages-of-git-integration).

After Source Control integration is defined, you can implement continuous integration and delivery by following the documentation about [Continuous integration and delivery in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment).
