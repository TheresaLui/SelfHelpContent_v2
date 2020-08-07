<properties
    pageTitle="Create read replicas in Azure Database for PostgreSQL"
    description="Create replicas"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="410"
    selfHelpType="generic"
    supportTopicIds="32639973"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9e065390-0a87-42d8-812b-39f24f7d04c7"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Create a replica

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

**Issue:** Preferred region not listed for replica.
The list of available cross-regions depends on your master server's region. Visit the read replica documentation for more information: https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#cross-region-replication. We are working to expand to more regions in the future.


**Issue:** The *Add Replica* button is disabled.

1. Refresh the *Replication* portal page
2. Confirm that you've selected *replica* or *logical* for your replication support level. [Learn more about these settings](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#prerequisites).
3. Restart the server

**Issue:** Replica creation is taking longer than expected.

Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your master server to the replica.

1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.postgres.database.azure.com`.
2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

## **Recommended Documents**

* [Restart your server](https://docs.microsoft.com/azure/postgresql/howto-restart-server-portal)
* [Create and manage read replicas in the portal](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
