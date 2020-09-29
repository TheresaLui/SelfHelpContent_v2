<properties
	pageTitle="Database connectivity - Proxy Throttling issue"
	description="Proxythrottle"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy"
	ms.author="subbuk"
	displayOrder=""
	articleId="IsProxyThrottling_0A86E0B4-1C26-4ACD-9B95-C6296829B8D8"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="31980402"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that connections utilizing the Proxy method of connecting to database  <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> were being throttled.  By default, connections originating outside of the Azure network boundary will use the proxy method which will be a shared common endpoint for connecting to the database(s) in that region. If performance regressions are seen or heavy traffic from a client are seen, throttling can occur.
<!--/issueDescription-->
## **Recommended Steps**

When using the proxy method, only the 1433 outbound port from the clients network needs to be allowed. Clients within Azure use the redirect method for authentication. While establishing a connection, this method provides a redirect token to the client, which includes the specific endpoint of the SQL database.  This instance will be listening on a dynamic port within the range of 11000-11999 and 14000-14999 which will require the network where the client resides to allow those outbound ports in addition to the standard 1433 port for SQL.

If this is causing issues for your application workload you can force all connections to your database to use the redirect method to connect, avoiding the potential of this scenario occurring.


## **Recommended Documents**
* [Azure SQL Database Connectivity Architecture](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture)
* [This article](https://docs.microsoft.com/azure/sql-database/sql-database-develop-direct-route-ports-adonet-v12)  discusses the port ranges for connections inside and outside of Azure due to the connection policy.   
