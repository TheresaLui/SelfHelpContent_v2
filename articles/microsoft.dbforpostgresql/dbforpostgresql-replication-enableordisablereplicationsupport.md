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

**Issue:** The *Disable Replication Support* button is not clickable.

The *Disable Replication Support* button controls the ability of the master server to send out data to any replica.

1. If you have an existing replica, you cannot disable replication support on the master
2. On Basic tier servers you cannot disable replication support, whether or not there is a replica
3. If the first two steps don't apply to you, refresh the Replication page to update the toolbar
4. If you want stop replication to an individual replica, making it a read/write server, [learn how to do so from the documentation](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal#stop-replication)

**Issue:** Cannot find the parameter `azure.replication_support` in the portal.

In the Azure portal, this setting is presented as the button *Enable Replication Support* or *Disable Replication Support* in the Replication page toolbar.

## **Recommended Documents**

* [Create and manage read replicas in the portal](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
