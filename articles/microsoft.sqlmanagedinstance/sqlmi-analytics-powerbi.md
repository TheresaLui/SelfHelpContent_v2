<properties
	pageTitle="Reporting Analytics Integration|PowerBI"
	description="Reporting Analytics Integration|PowerBI"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637292"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    articleId="fce8eb20-3991-47a2-836a-20c66464fd1d"
	ownershipId="AzureData_AzureSQLMI"
/>

# PowerBI

Azure SQL Managed Instance is a cloud service injected into customer's VNet and by default not available from the PowerBI Online.
There are two approaches for enabling managed instance as a PowerBI data source.

## **Recommended Steps**

- Use [on-premises data gateway](https://docs.microsoft.com/power-bi/service-gateway-onprem) to reach VNet-injected managed instance
- [Configure public endpoint in managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-public-endpoint-configure)