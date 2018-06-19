<properties
	pageTitle="How to troubleshoot connection issues with SQL Data Warehouse"
	description="How to connect"
	service="microsoft.sql"
	resource="servers"
	authors="kevinvngo"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32412140, 32412141, 32412143, 32412144, 32412155, 32589561, 32412153, 32412154, 32412159"
	resourceTags="datawarehouse"
	productPesIds="15818"
	cloudEnvironments="public"
/>

## How to troubleshoot connection and tooling issues with SQL Data Warehouse

## **Recommended steps**

Issues with connecting to SQL Data Warehouse can occur due to a number of issues including incorrect firewall configuration, connection strings, or maintenance periods.  If you are having issues with a client tool, please ensure you have the latest version of the tool and [visit the following documentation](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot#tools). 

1. Check the [Resource Health Check](https://docs.microsoft.com/azure/service-health/resource-health-overview) for this data warehouse and [Microsoft Azure Service Dashboard](https://azure.microsoft.com/status/) for any known issues.
2. Set-up firewall rules to allow the client IP address.<br>
  [Configure SQL Azure firewall rules](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-get-started-provision/#create-a-new-azure-sql-server-level-firewall)
3. See how to discover connection string from the portal.<br>
  [Connect to Azure SQL Data Warehouse](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-connect-overview/)
4. View connection string format.<br>
  [Connection Strings](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-connection-strings/)

## **Recommended documents**
[Additional Troubleshooting](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)
