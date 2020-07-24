<properties
    pageTitle="App Service operator installation and upgrade SQL Always On"
    description="App Service operator installation and upgrade SQL Always On"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="BryanLa"
    ms.author="bryanla"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32742870"
    resourceTags=""
    productPesIds="17136"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="appserviceazurestackhub-operator-installationandupgrade-sql-always-on"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# App Service operator installation and upgrade SQL Always On

## **Recommended Steps**

The SQL Server instance must be accessible from all App Service roles, as well as the App Service resource provider (RP) blade in the administrator portal.

### 1. Verify completion of prerequisites and post-deployment steps

Confirm that you've followed the [deployment prerequisites](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started), and [post-deployment steps](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-deploy?pivots=state-connected#post-deployment-steps), specifically:

- If you didn't deploy SQL Server using the [Quickstart template for Highly Available file server and SQL Server](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started#quickstart-template-for-highly-available-file-server-and-sql-server), review [Prepare the SQL Server instance](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started#prepare-the-sql-server-instance) to ensure your SQL Server is deployed in a highly available configuration and configured correctly. 

- For production deployments, SQL Server must be configured to be highly available and capable of handling failures, using the SQL Always On feature. Following deployment of the App Service resource provider, you must also [add the appservice_hosting and appservice_metering databases to an Always On availability group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-add-a-database), and synchronize the databases to prevent any loss of service in the event of a database failover. 

### 2. Verify SQL Server database instance is reachable from the App Service RP blade

Open the App Service RP blade in the Azure Stack Hub administrator portal. If you see a raining cloud image with text *"Failed to load App Service extension. Please check whether App Service resource provider and sql database is up and running"*, the database is not reachable.

If you deployed SQL Server using the "Quickstart template for Highly Available file server and SQL Server", the SQL Server databases were deployed to Azure Stack Hub as part of the App Service installation. Complete the following steps to determine whether you can restart the SQL Server instance:
**ADD MORE DIAGNOSTIC STEPS HERE? OR CONTACT CSS?**

If you provided your own SQL Server databases during deployment, you'll need to complete additional diagnosis to determine why SQL Server cannot be reached.

### 3. Verify whether the SQL Server SA password was changed

SA password change can cause this too; might be other log messages that would give clues as to why SQL can’t be contacted.

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)

