<properties
    pageTitle="Connection failures to PostgreSQL"
    description="Connection failures to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32789520"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="0663a2af-a594-4c37-9a26-eacadb5ac87d"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **All connections to PostgreSQL Flexible Server are failing suddenly**
## **Recommended Steps**

The cause may be an issue in Azure infra-structure or ongoing/scheduled maintenance activities.

- There may be a planned maintenance activity going on your database server. Check the **Resource Health** for the status. We recommend setting up [custom maintenance window](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-maintenance-portal) that aligns with your workload pattern.
- Check the **Resource health** for your server to see if there were any reported events that could have caused the connection disruption
- Check the **Activity log** for your server to see if there are changes to the server that could have causes the connection drops
- Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, please review your client's timeout settings.

## **Recommended Documents**

- [Troubleshoot common connectivity issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
- [Manage scheduled maintenance settings for Azure Database for PostgreSQL – Flexible server](https://docs.microsoft.com/azure/postgresql/flexible-server/how-to-maintenance-portal)