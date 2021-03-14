<properties
	pageTitle="Other Migration Issues to Azure SQL DB Managed Instance"
	description="Other Migration Issues for Azure SQL DB Managed Instance"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="migration-errors-other-sqldbmi"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743211"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting migration failures 

For information about DMS prerequisites, service instances, configuring migration projects, and troubleshooting errors: Go to the Azure Database Migration Service Documentation website, and search for the **How-to Guides, Tutorials, and Resources** section.


### Troubleshooting the error when more than the maximum number of databases are selected for migration  

* See [Troubleshoot max number of databases selected for migration](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#max-number-of-databases-selected-for-migration)

* If you get the error, "Service has reported errors when trying to migrate more than 4DBs per service":

   * The Service can only migrate 4 DBs concurrently and you can have 2 services per subscription
   * DMS only supports 4 DBs to migrate concurrently. It allows you to create many projects, for example, you create 10 projects and select 4 databases in each. Although you have 40 Dbs but only 4 of them will be migrated at one time.
   * Another limit is per sub, per region. Only 2 DMS services are allowed to create, which means you'll have 8 DBs to migrate concurrently

### Migration Activity in Queued State

* [Troubleshooting migration activity in queued state](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#migration-activity-in-queued-state)<br>

### Validation error when having many roles assigned to a resource

* When multiple roles are assigned to a resource (such as the storage account which is required for uploading the backup files from the SMB network share in the MI migration process), the most restrictive role gets applied for the Service Principal. This usually results in an "insufficient permissions" error during the validation step. Grant only the Contributor role to the AppID used for the MI migration. Refer to the documentation on [MI pre-requisites](https://docs.microsoft.com/azure/dms/tutorial-sql-server-managed-instance-online#prerequisites) for more information.

## **Recommended Documents**

* [Azure Database Migration Service Documentation](https://docs.microsoft.com/azure/dms/)
* [Troubleshoot common Azure DMS issues and errors](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)
