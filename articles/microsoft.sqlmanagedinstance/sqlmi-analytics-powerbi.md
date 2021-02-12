<properties
  pagetitle="PowerBI"
  service="microsoft.sql"
  resource="managedinstances"
  ms.author="mlazic,katmac"
  selfhelptype="Generic"
  supporttopicids="32637292"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="fce8eb20-3991-47a2-836a-20c66464fd1d"
  ownershipid="AzureData_AzureSQLMI" />
# PowerBI

Azure SQL Managed Instance is a cloud service injected into customer's VNet and by default not available from the PowerBI Online.
There are two approaches for enabling managed instance as a PowerBI data source.

## **Recommended Steps**

- Use [on-premises data gateway](https://docs.microsoft.com/power-bi/service-gateway-onprem) to reach VNet-injected managed instance
- [Configure public endpoint in managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-public-endpoint-configure)
- [Integrate Microsoft cloud services with your Azure SQL Database managed instance](https://techcommunity.microsoft.com/t5/azure-sql-database/integrate-microsoft-cloud-services-with-your-azure-sql-database/ba-p/1083543)