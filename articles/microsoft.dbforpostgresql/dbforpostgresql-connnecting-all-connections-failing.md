<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32788700, 32789526"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ef16f51c-b0b5-46b4-accf-3f022b9fd1c9"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **All connections to PostgreSQL are failing suddenly**
## **Recommended Steps**


The cause may be an issue in Azure infra-structure or ongoing/scheduled maintenance activities.

- There may be a planned maintenance activity going on your database server. Check the **Resource Health** for the status. We recommend setting up [planned maintenance notifications](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification) to get advance notification of maintenance activity.
- Check the **Resource health** for your server to see if there were any reported events that could have caused the connection disruption
- Check the **Activity log** for your server to see if there are changes to the server that could have causes the connection drops
- Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, please review your client's timeout settings.
- If you think there is a regional outage, see [Overview of business continuity](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity) with Azure Database for PostgreSQL for steps to recover to a new region.

## **Recommended Documents**

- [Troubleshoot common connectivity issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
- [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
- [Understanding the connectivity architecture for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
