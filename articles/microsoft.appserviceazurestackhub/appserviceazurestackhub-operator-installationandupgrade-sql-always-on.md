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

### Verify completion of installation prerequisites

First, make sure you've followed the prerequisites outlined in [Prerequisites for deploying App Service on Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started). 

### Verify SQL Server deployment in a highly available configuration

If you deployed SQL Server using the [Quickstart template for Highly Available file server and SQL Server](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started#quickstart-template-for-highly-available-file-server-and-sql-server), you can skip this section. 

If you did not use the template, and deployed App Service using your own SQL Server database, be sure to review [Prepare the SQL Server instance](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started#prepare-the-sql-server-instance) to ensure SQL Server is deployed in a highly available configuration. 

### Verify SQL Server Always On instance belongs to an availability group

For production deployments, SQL Server must be configured to be highly available and capable of handling failures. If you've provided the App Service resource provider with a SQL Always On server instance, you must [add the appservice_hosting and appservice_metering databases to an Always On availability group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-add-a-database), and synchronize the databases to prevent any loss of service in the event of a database failover. 

## Resolve "can't be reached" or "can’t reach database" status in administrator portal

Confirm whether the SQL Server database instance is reachable, by opening the App Service RP blade in the Azure Stack Hub administrator portal. If you see a raining cloud image with text *"Failed to load App Service extension. Please check whether App Service resource provider and sql database is up and running"*, the database is not reachable.

If you provided your own SQL Server databases during deployment, you'll need to complete additional diagnosis to determine why SQL Server cannot be reached..

If you deployed SQL Server using the "Quickstart template for Highly Available file server and SQL Server", the SQL Server databases were deployed to Azure Stack Hub as part of the App Service installation. Complete the following steps to determine whether you can restart the SQL Server instance:
**ADD MORE DIAGNOSTIC STEPS HERE**

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)

