<properties
    pageTitle="Troubleshooting maximum connection limit in Azure Database for MySQL"
    description="Troubleshooting maximum connection limit in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="60"
    selfHelpType="generic"
    supportTopicIds="32640091"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="eb1a77db-8690-408d-a3a7-4b8ff48edd78"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting maximum connection limit in Azure Database for MySQL

Each active connection consumes memory and therefore the maximum number of connections allowed depends upon the chosen pricing tier. Higher pricing tiers have more  memory and hence higher limits on maximum connections

## **Recommended Steps**

* Ensure you have chosen the appropriate pricing tier that can support the maximum number of connections required by the application
* Try to reduce the number of concurrent connections by closing idle connections or better by using connection pooling on the client

## **Recommended Documents**

* [MySQL Max connections](https://docs.microsoft.com/azure/mysql/concepts-limits)<br> 
* [Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/)
