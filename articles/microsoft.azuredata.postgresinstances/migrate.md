<properties
	pageTitle="Migrate Data into Azure Arc"
	description="Migrate Data into Azure Arc"
	infoBubbleText="Migrate Data into Azure Arc"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="32e37b98-f7c9-4b5a-aa5a-601b54a90fe7"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747910"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
    
# Migrate Database into Azure Arc

## **Recommended Steps**

* It is not possible today to onboard into Azure Arc an existing Postgres setup that would running on-prem or in any other cloud
* In other words it is not possible to install some sort of "Azure Arc agent" on your existing Postgres setup to make it a Postgres setup enabled by Azure Arc. Instead, you need to deploy a new Postgres instance and transfer data into it.

## **Recommended Documents**

- [Migrating data into Azure Arc enabled Postgres Hyperscale](https://docs.microsoft.com/azure/azure-arc/data/migrate-postgresql-data-into-postgresql-hyperscale-server-group)  
- [Restore AdventureWorks sample DB "restoring" by recreating objects and importing data](https://docs.microsoft.com/azure/azure-arc/data/restore-adventureworks-sample-db-into-postgresql-hyperscale-server-group) 
- [Ora2pg](https://ora2pg.darold.net/)
- [Storage configuration](https://docs.microsoft.com/azure/azure-arc/data/storage-configuration)
