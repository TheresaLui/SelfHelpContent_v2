<properties
    pageTitle="Configuring replication support in Azure Database for PostgreSQL"
    description="Errors with enabling or disabling replication support"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32639976"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="48a86109-e938-4adf-8030-3b7548e3e838"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Enable or disable replication support

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

Issue: Not sure **whether to choose *replica* or *logical*** for Azure replication support
   * Choose *replica* if you are only creating read replicas
   * Choose *logical* if you are using [logical decoding](https://docs.microsoft.com/azure/postgresql/concepts-logical)
   * Learn more about the [Azure replication support setting](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#prerequisites)

Issue: Interested in **logical replication**
   * Logical replication with Azure Database for PostgreSQL as a subscriber is not supported
   * Logical replication is a different PostgreSQL feature from [logical decoding](https://docs.microsoft.com/azure/postgresql/concepts-logical)

Issue: Want to **stop replication to a replica**
   * Visit our [stop replication guide](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#stop-replication)

Issue: **Replication setting on a replica**
   * You cannot change the Azure replication support setting on a read replica

Issue: Cannot **find the parameter `azure.replication_support`** in the portal.

   * In the Azure portal, this setting is available in the *Replication* page for the server.


## **Recommended Documents**

* [Create and manage read replicas in the portal](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
