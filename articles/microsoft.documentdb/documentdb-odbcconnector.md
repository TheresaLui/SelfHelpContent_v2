<properties
	pageTitle="Cosmos DB ODBC Connector"
	description="Cosmos DB ODBC Connector"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="92"
	selfHelpType="resource"
	supportTopicIds="32597560"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# Azure Cosmos DB ODBC Connector

## **Recommended Steps**
The Azure Cosmos DB ODBC driver enables you to connect Azure Cosmos DB to BI analytics tools such as SQL Server Integration Services, Power BI Desktop, and Tableau so that you can analyze and create visualizations of your Azure Cosmos DB data in those solutions.
The Azure Cosmos DB ODBC driver is ODBC 3.8 compliant and supports ANSI SQL-92 syntax. The driver offers rich features to help you renormalize data in Azure Cosmos DB. Using the driver, you can represent data in Azure Cosmos DB as tables and views. The driver enables you to perform SQL operations against the tables and views including group by queries, inserts, updates, and deletes.

### **Troubleshooting**

* Currently, connecting to Azure Cosmos DB with the ODBC driver is  supported for Azure Cosmos DB SQL API accounts only.
* If you receive an authorization error, ensure that the Host and Access key values are correctly set. The Host should be the URI for the Azure Cosmos DB account and the Access Key should be the primary or secondary key obtained from the Azure Cosmos DB Keys page. 

## **Recommended Documents**
* [Azure Cosmos DB ODBC driver documentation](https://docs.microsoft.com/azure/cosmos-db/odbc-driver)
* [Azure Cosmos DB PowerBI Connector](https://docs.microsoft.com/azure/cosmos-db/powerbi-visualize)
