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
  diagnosticScenario="crc_sqldb_connectivity"
  selfHelpType="diagnostics"
  supportTopicIds="32630429"
  resourceTags=""
  productPesIds="13491"
  cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
As part of Azure infrastructure improvements we upgraded some of our clusters to newer hardware across all regions. Server <!--$ServerName-->ServerName<!--/$ServerName--> was a part of this migration. This migration will change the public IP address that DNS resolves for your SQL Database. You must have received email communications related to this migration dated September 13th, 2019.

You will be impacted:
*  If you have not hard coded the new IP addresses as the documentation below.
*  If you have subnets using Microsoft.SQL as a Service Endpoint but unable to communicate the source IP of SQL.

You will not be impacted if you have:
*  Redirection as the connection policy.
*  Connections to SQL Database from inside Azure and using Service Tags. 

<!--/issueDescription-->

## **Recommended Steps**

* Update your outgoing firewall rules (on your client machine and/or network) to include the newer IP addresses. Refer the link below for new IP addresses.

## **Recommended Documents**

* [Gateway Migration to new hardware ](https://docs.microsoft.com/azure/sql-database/sql-database-gateway-migration)
* [Connection policy for Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture#connection-policy)
* [Azure SQL Database gateway IP Addresses](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture#azure-sql-database-gateway-ip-addresses)
