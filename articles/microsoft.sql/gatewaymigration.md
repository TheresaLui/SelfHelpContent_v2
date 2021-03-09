<properties
  pageTitle="SQL Gateway Migration"
  description="SQL Gateway Migration"
  infoBubbleText="Found recent connectivity issue. See details on the right."
  service="microsoft.sql"
  resource="servers"
  authors="subbu-kandhaswamy, swbhartims"
  ms.author="subbuk, swbharti"
  displayOrder=""
  articleId="GatewayMigration_257E0082-CAC5-4934-812E-AC8DA79D9318"
  diagnosticScenario="SqlConnectivity"
  selfHelpType="diagnostics"
  supportTopicIds="32630429, 32635195"
  resourceTags=""
  productPesIds="13491, 15818"
  cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
As part of Azure infrastructure improvements, we upgraded some of our clusters to newer hardware across all regions. Server <!--$ServerName-->ServerName<!--/$ServerName--> was a part of this migration. This migration will change the public IP address that DNS resolves for your SQL Database. We send proactive communications on this migrations to subscription owners for this region and you must have received email communications related to this migration.  

<!--/issueDescription-->

If you are experiencing connectivity issues, it could be related to this migration. Please ensure that:

1. You have updated any outgoing firewall rules (on your client machine and/or network) to include the newer IP addresses using this [table](https://docs.microsoft.com/azure/azure-sql/database/connectivity-architecture#gateway-ip-addresses)
2. You have updated your Network Security Groups (NSGs) to include the newer IP address using this [table](https://docs.microsoft.com/azure/azure-sql/database/connectivity-architecture#gateway-ip-addresses), if you are using Microsoft.SQL as a Service Endpoint

## **Recommended Steps**

1. Ensure that you do not have any hard-coded IP addresses in your outgoing firewall rules or any other outbound network restrictions in your environment
2. Ensure to include the newer IP addresses to your NSGs, as per the documentation below

## **Recommended Documents**

* [Gateway Migration to new hardware](https://docs.microsoft.com/azure/sql-database/sql-database-gateway-migration)
* [Connection policy for Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture#connection-policy)
* [Azure SQL Database gateway IP Addresses](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture#azure-sql-database-gateway-ip-addresses)
