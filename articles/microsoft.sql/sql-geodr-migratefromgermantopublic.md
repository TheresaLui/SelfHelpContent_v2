<properties
	pageTitle="Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure"
	description="Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure"
	service="microsoft.sql"
	resource="servers"
	authors="subbuk"
	authoralias="subbuk"
	ms.author="subbuk"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32785509, 32785645"
	productPesIds="13491, 15660"
	cloudEnvironments="blackForest"
	articleId="427a0459-7468-49d0-9da5-111aa863ecfe"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure

## **Recommended Steps**

The best method for migrating your database depends on the database size and availability requirements.  Smaller databases can be migrated during a downtime window by exporting to a .bacpac file and then importing the .bacpac to the new server. Larger databases, or scenarios where you must minimize downtime, are best migrated using active geo-replication.

Establishing a geo-replication link from the Azure Germany cloud to a server on Azure Global (public cloud) requires that you add allow list each target subscription.  Allow list requests must be submitted from the Azure Germany (source) subscription.  If you are replicating the databases to different target subscriptions you can enter multiple subscriptions in a single request. You will be prompted to enter the desired target, subscription ID(s) on the next tab.   

After your allow list request is processed, migrate your database using the following documents.


## **Recommended Documents**
* [Migrate database using active Geo Replication](https://docs.microsoft.com/azure/germany/germany-migration-databases?branch=pr-en-us-138592#migrate-sql-database-using-active-geo-replication)
* [Microsoft Cloud Deutschland transition](https://www.microsoft.com/cloud-platform/germany-cloud-regions)
* [Migrate database resources to Azure Global](https://docs.microsoft.com/azure/germany/germany-migration-databases?branch=pr-en-us-138592)
