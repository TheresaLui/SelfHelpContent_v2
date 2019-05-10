<properties
	pageTitle="Configuring replication support in Azure Database for PostgreSQL"
	description="Errors with enabling or disabling replication support"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="rachel-msft"
    ms.author="raagyema"
	displayOrder="53"
	selfHelpType="resource"
	supportTopicIds="32639976"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="postgresconfigurereplicationsupport"
/>

# Replication support

Most users are able to resolve their issue using the steps below.

## **Recommended steps**

**Issue:** The *Disable Replication Support* button is not clickable.

The *Disable Replication Support* button controls the ability of the master server to send out data to any replica.

1. If you have an existing replica, you cannot disable replication support on the master. 

2. On Basic tier servers you cannot disable replication support, whether or not there is a replica.

3. If the first two steps don't apply to you, refresh the Replication page to update the toolbar.

4. If what you want to do is stop replication to an individual replica, making it a read/write server, [learn how to do so from the documentation](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal#stop-replication). 



**Issue:** Cannot find the parameter `azure.replication_support` in the portal.

In the Azure portal, this setting is presented as the button *Enable Replication Support* or *Disable Replication Support* in the Replication page toolbar.

## **Recommended documents**

* [How to create and manage read replicas in the portal](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal)

* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)

* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
