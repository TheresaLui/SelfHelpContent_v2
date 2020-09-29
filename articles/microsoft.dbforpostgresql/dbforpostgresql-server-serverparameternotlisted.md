<properties
    pageTitle="Server parameter not listed"
    description="Guidance on what to do when a server parameter is not listed"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="500"
    selfHelpType="generic"
    supportTopicIds="32640021"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7ab60a0b-a8a1-4cfc-ac41-e91105b4102f"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Server parameter not listed

Azure Database for PostgreSQL allows you to configure parameters at a server level using the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal) or the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-cli). 

To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal. Not all PostgreSQL parameters are available for you to reconfigure in Azure Database for PostgreSQL. If a PostgreSQL parameter is not listed in your server's Azure portal **Server parameters** window, then it cannot be reconfigured from the default.

## **Recommended Steps**

* If a parameter you'd like to configure is not listed, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/597976-azure-database-for-postgresql).  We evaluate these requests periodically and make parameters configurable if we can safely do so.

## **Recommended Documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal)<br>
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-cli)
