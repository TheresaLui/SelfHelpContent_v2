<properties
	pageTitle="How to troubleshoot connection issues with SQL Data Warehouse"
	description="How to connect"
	service="microsoft.sql"
	resource="servers"
	authors="kevinvngo"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="datawarehouse"
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# How to troubleshoot connection and tooling issues with your data warehouse

## **Recommended steps**

Issues with connecting to SQL Data Warehouse can occur due to a number of issues including incorrect firewall configuration, connection strings, or maintenance periods.  If you are having issues with a client tool, please ensure you have the latest version of the tool and [visit the following documentation](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot#tools). 

1. Check the [Resource Health Check](https://docs.azure.cn/service-health/resource-health-overview) for this data warehouse and [Microsoft Azure Service Dashboard](https://www.azure.cn/support/service-dashboard/) for any known issues.
2. [Set up firewall rules](https://docs.azure.cn/sql-data-warehouse/create-data-warehouse-portal#create-a-server-level-firewall-rule) to allow the client IP address.
3. See how to [find the connection string](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-connect-overview#find-your-server-name) from the portal.
4. View the [connection string format](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-connection-strings).

## **Recommended documents**

* [Additional Troubleshooting](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-troubleshoot/)
