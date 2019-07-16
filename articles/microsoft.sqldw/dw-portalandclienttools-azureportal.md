<properties
	pageTitle="Specific errors or exceptions"
	description="Specific errors or exceptions"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,mlee3gsd"
	ms.author="saltug,martinle"
	supportTopicIds="32635189"
	productPesIds="15818"
	displayOrder="31"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-portalandclienttools-azureportal.md"
	cloudEnvironments="public"
/>

# Using the Azure Portal

## **Recommended Steps**

* When using the Azure Portal Query Editor, review the following [documentation](https://docs.microsoft.com/azure/sql-database/sql-database-connect-query-portal#query-editor-considerations)
* The following limitations exists with the portal query editor:

    * There's a 5-minute timeout for query execution
    * You can't use the query editor in a Virtual Network
    * Pressing F5 refreshes the query editor page and any queries being worked on is lost
    * Query editor doesn't support connecting to the master database

