<properties
  pageTitle="Firewall  issues connecting to SQL Database"
  description="Firewall Issue Blocking connectivity to SQL Database"
  infoBubbleText="Firewall Issue Blocking connectivity to SQL Database."
  service="microsoft.sql"
  resource="servers"
  authors="subbu-kandhaswamy"
  ms.author="subbuk"
  displayOrder=""
  articleId="Isfirewallerror_ecae0028-f6a9-4b30-bea1-ee242dea9d56"
  diagnosticScenario="crc_sqldb_connectivity"
  selfHelpType="rca"
  supportTopicIds="32745431"
  resourceTags=""
  productPesIds="13491"
  cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC, connection(s) to the database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName-->, by the requesting client IP address was not allowed due to the existing firewall rule.

This occurs when a client computer attempts to connect your server from on-premises or from Azure Services (Web App or from a virtual machine), and the IP address of the client is not within a range of any of the database-level or server-level IP firewall rules. In this case, the connection request fails.

The firewall configuration varies, depending on whether the client is connecting from inside or outside of Azure.

If you're connecting from **on-premises** (your local machine) to Azure SQL DB, ensure that the firewall on your network and local computer allows outgoing communication on TCP port 1433.

If your application or client is connecting from **inside Azure**, the firewall verifies that Azure connections are allowed. You can turned this on (allow) directly from the Azure portal blade by setting firewall rules, and by switching the Allow Azure Services and resources to access this server to **On** in the firewall and virtual networks settings.

For more information on how to configure firewall rules, see the following documents.

<!--/issueDescription-->

## **Recommended Documents**

* [Configuring IP Firewall Rules](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure#troubleshoot-the-database-firewall)
* [Virtual Network (VNET) settings](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview)
* [Firewall considerations for private endpoints ](https://docs.microsoft.com/azure/azure-sql/database/private-endpoint-overview)
* [Troubleshooting Firewall Issues](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure#troubleshoot-the-database-firewall)
