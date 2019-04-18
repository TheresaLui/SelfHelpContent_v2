<properties
	pageTitle="Create read replicas in Azure Database for PostgreSQL"
	description="Create replicas"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="rachel-msft"
    ms.author="raagyema"
	displayOrder="40"
	selfHelpType="resource"
	supportTopicIds="32633544"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="postgrescreatereplica"
/>

# Create a replica

Most users are able to resolve their issue using the steps below.

## **Recommended steps**

**Issue:** The *Add Replica* button is disabled.

1. Refresh the *Replication* portal page.
2. Confirm that the *Enable Replication Support* option is unavailable. This indicates that replication is already enabled for this server.
3. Restart the server.


**Issue:** Replica creation is taking longer than expected.

Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your master server to the replica.

1. Using a shell, ping the DNS of the replica. For example, if you named the replica 'myreplica', the DNS name is myreplica.postgres.database.azure.com. 
2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.


## **Recommended documents**

* [How to restart your server](https://docs.microsoft.com/azure/postgresql/howto-restart-server-portal)

* [How to create and manage read replicas in the portal](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal)

* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)

* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)


