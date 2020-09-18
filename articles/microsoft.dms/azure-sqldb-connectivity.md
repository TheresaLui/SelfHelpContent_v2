<properties
	pageTitle="Errors in connectivity for Azure SQL DB"
	description="Connectivity errors for Azure SQL DB"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="azure-sqldb-connectivity"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743198"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting DMS database connectivity issues 

## Errors Connecting to Target

## **Recommended Documents**

* [Troubleshoot connection issues to Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-troubleshoot-common-connection-issues)<br>
* [Azure SQL Database Managed Instance Connectivity Architecture](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture)

## Errors Connecting to Source

## **Recommended Documents**

* [Troubleshoot DMS errors when connecting to source databases](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms-source-connectivity)

## Errors you may encounter with firewall rules and network configuration 

## **Recommended Steps**

**Connection error when using ExpressRoute**

When you try to connect to source in the Azure Database Migration service project wizard, the connection fails after prolonged timeout if source is using ExpressRoute for connectivity.

See here for causes and troubleshooting info:
[Connection error when using ExpressRoute](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#connection-error-when-using-expressroute)

## **Recommended Documents**

* [DMS known issues and troubleshooting](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)

## General Guidelines

See How-to Guides, Tutorials, and Resources section in Azure Database Migration Service documentation for DMS service pre-requisites, instance settings, configuring migration projects, and troubleshooting errors.

## **Recommended Documents**

* [Azure Database Migration Service Documentation](https://docs.microsoft.com/azure/dms/)