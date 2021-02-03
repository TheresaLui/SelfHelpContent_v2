<properties
	pageTitle="Backup Restore Arc"
	description="Backup and Restore for Azure Database for PostgreSQL Hyperscale server groups"
	infoBubbleText="Backup & Restore PostgreSQL Hyperscale Server Group"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="4e27e016-24c1-48b9-b191-2a92561f03da"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747898"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>

# Backup and Restore for Azure Database for PostgreSQL Hyperscale server groups

Most users are able to resolve backup restore related questions and issues using the below steps.

## **Recommended Steps**

* You can do full backup/restore of your Azure Arc enabled PostgreSQL Hyperscale servergroup. When you do so, the entire set of databases on all the nodes of your Azure Arc enabled PostgreSQL Hyperscale servergroup is backed-up and restored. 
* To take a backup and restore it, you need to make sure that a backup storage class is configured for your PostgreSQL servergroup. For now this needs to be set at the time you create the servergroup. It is not yet possible to configure your servergroup to use a backup storage class after it has been created.
* Read about [Backup and restore on Azure Arc](https://docs.microsoft.com/azure/azure-arc/data/backup-restore-postgresql-hyperscale)
* It is not possible today to "onboard into Azure Arc" an existing Postgres setup that would running on-prem or in any other cloud
* In other words it is not possible to install some sort of "Azure Arc agent" on your existing Postgres setup to make it a Postgres setup enabled by Azure Arc. Instead, you need to deploy a new Postgres instance and transfer data into it.

## **Recommended Documents**

- [Migrating data into Azure Arc enabled Postgres Hyperscale](https://docs.microsoft.com/azure/azure-arc/data/migrate-postgresql-data-into-postgresql-hyperscale-server-group)  
- [Restore AdventureWorks sample DB "restoring" by recreating objects and importing data:](https://docs.microsoft.com/azure/azure-arc/data/restore-adventureworks-sample-db-into-postgresql-hyperscale-server-group) 
- [Storage configuration](https://docs.microsoft.com/azure/azure-arc/data/storage-configuration)
