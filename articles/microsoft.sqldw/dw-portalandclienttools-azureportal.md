<properties
    pageTitle="Troubleshooting Azure Portal"
    description="Troubleshooting Azure Portal"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635189"
    productPesIds="15818"
    displayOrder="62"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-portalandclienttools-azureportal.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Using the Azure Portal

## **Recommended Steps**

* To create and query a data warehouse using Azure Portal, see [steps outlined here](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal).
* Azure Portal and Azure SQL Data Warehouse credentials are not the same. To see the admin login, click on the Properties tab on your Azure SQL Data Warehouse page on Azure Portal.
* When using the Azure Portal Query Editor, review the following [documentation](https://docs.microsoft.com/azure/sql-database/sql-database-connect-query-portal#query-editor-considerations)
* [ARM tags](https://docs.microsoft.com/azure/azure-resource-manager/tag-support#sqlnote) can only be applied to an active SQL Data Warehouse
* The following limitations exists with the portal query editor:
  * There's a 5-minute timeout for query execution
  * You can't use the query editor in a Virtual Network
  * Pressing F5 refreshes the query editor page and any queries being worked on is lost
  * Query editor doesn't support connecting to the master database
