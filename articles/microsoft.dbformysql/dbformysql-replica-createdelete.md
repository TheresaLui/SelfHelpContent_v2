<properties
	pageTitle="Create read replicas in Azure Database for MySQL"
	description="Create replicas"
	service="microsoft.dbformysql"
	resource="servers"
	authors="ajlam"
    ms.author="andrela"
	displayOrder="54"
	selfHelpType="resource"
	supportTopicIds="32640050"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="mysqlcreatereplica"
/>

# Create a replica

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

**Issue:** Replica creation is taking longer than expected.

Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your master server to the replica.

1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.mysql.database.azure.com`.
2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

## **Recommended Documents**

* [Create and manage read replicas in the portal](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/mysql/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/mysql/concepts-read-replicas)