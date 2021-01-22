<properties
    pageTitle="High availability for Azure Database for PostgreSQL - flexible server"
    description="High availability for Azure Database for PostgreSQL - flexible server"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32780965, 32780977"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-availability-highavailability"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# High availability - Azure Database for PostgreSQL Flexible Server

Azure Database for PostgreSQL - Flexible Server offers high availability configuration with automatic failover capability using zone-redundant server deployment. When deployed in a zone-redundant configuration, a flexible server automatically provisions and manages a standby replica in a different availability zone. Using PostgreSQL streaming replication, the data is replicated to the standby replica server in synchronous mode.

## **Recommended Steps**
* You can choose the region and the availability zone to deploy your primary database server. A standby replica server is provisioned in a different availability zone with the same configuration as the primary server, including compute tier, compute size, storage size, and network configuration.
* High availability is not supported with burstable compute tier
* High availability is supported only in regions where multiple zones are available
* Due to synchronous replication to another availability zone, applications can experience elevated write and commit latency
* Standby replica cannot be used for read-only queries
* Depending on the activity on the primary server at the time of failover, it might take up to two minutes or longer for the failover to complete
* Restarting the primary database server to pick up static parameter changes also restarts the standby replica
* Planned events, such as scale compute and scale storage, happen in the standby first, and then on the primary server. The service is not failed over.
