<properties
	pageTitle="Availability and Connectivity/Power BI connections to Azure Synapse Analytics with Azure AD Authentication"
	description="Availability and Connectivity/Power BI connections to Azure Synapse Analytics with Azure AD Authentication"
	service="microsoft.sql"
	resource="servers"
	authors="nanditavalsan"
	ms.author="nanditav@microsoft.com"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="dw-availabilityandconnectivity-azureactivedirectoryauthentication-powerbi.md"
	ownershipId=""
/>

# <Power BI connections to Azure Synapse Analytics with Azure AD Authentication>

For the best experience to connect to your Azure Synapse Analytics data warehouse data source, use Power BI Desktop. Once you've built your model and report, you can publish it to the Power BI service. 

## **Power BI Integration**
Power BI integration currently includes:

1. Direct Connect: A more advanced connection with logical pushdown against a data warehouse provisioned using SQL pool. Pushdown provides faster analysis on a larger scale. DirectQuery always uses the same fixed credentials to connect to the underlying data source, after it's published to the Power BI service.The same attention must be paid to sharing the report, if there are any security rules defined in the underlying source.
2. Open in Power BI (recommended): The 'Open in Power BI' button passes instance information to Power BI for a simplified way to connect. [Using the 'Open in Power BI' button](https://docs.microsoft.com/power-bi/service-azure-sql-data-warehouse-with-direct-connect#using-the-open-in-power-bi-button)

## **Recommended Steps**

1. [Data sources in Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-data-sources)
2. [Azure SQL Data Warehouse with DirectQuery](https://docs.microsoft.com/power-bi/service-azure-sql-data-warehouse-with-direct-connect) for Azure Synapse Analytics


## **Recommended Documents**

* [Troubleshooting scheduled refresh for Azure SQL Databases in Power BI](https://docs.microsoft.com/power-bi/service-admin-troubleshooting-scheduled-refresh-azure-sql-databases)
* [Single Sign On via Azure AD for Azure Synapse Analytics and Power BI](https://docs.microsoft.com/power-bi/service-azure-sql-data-warehouse-with-direct-connect#single-sign-on)
* [When is DirectQuery useful?](https://docs.microsoft.com/power-bi/desktop-directquery-about#when-is-directquery-useful)


