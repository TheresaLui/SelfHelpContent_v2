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

Azure Database for PostgreSQL - Flexible Server offers high availability configuration with automatic failover capability using zone-redundant server deployment. You may be able to find answers to most of your HA related questions.

## Frequently asked questions

* **How does flexible server provide high availability in the event of a fault - like AZ fault?** <br>
When you enable your server with zone-redundant HA, a physical standby replica with the same compute and storage configuration as the primary is deployed automatically in a different availability zone than the primary. PostgreSQL streaming replication is established between the primary and standby servers. 

* **Is zone redundant HA available in all regions?** <br>
Zone-redundant HA is available in regions that support multiple AZs in the region. For the latest region support, please see [this documentation](https://docs.microsoft.com/azure/postgresql/flexible-server/overview#azure-regions). We are continuously adding more regions and enabling multiple AZs. 

* **What mode of replication is between primary and standby servers?** <br>
Synchronous mode of replication is established between the primary and the standby server. Application writes and commits are acknowledged only after the Write Ahead Log (WAL) data is persisted on the standby site. This enables zero data loss in the event of a failover.

* **Synchronous mode incurs latency. What kind of performance impact I can expect for my application?** <br>
Configuring in HA induces some latency to writes and commits. No impact to read queries. The performance impact varies depending on your workload. As a general guideline, writes and commit impact can be around 20-30% impact. 

* **Does the zone-redundant HA provides protection from planned and unplanned outages?** <br>
Yes. The main purpose of HA is to offer higher uptime to mitigate from any outages. In the event of an unplanned outage - including a fault in database, VM, physical node, data center, or at the AZ-level, the monitoring system automatically fails over the server to the standby. Similarly, during planned outages including minor version updates or infrastructure patching that happen during scheduled maintenance window, the updates are applied at the standby first and the service is failed over while the old primary goes through the update process. This reduces the overall downtime. 

* **What is the typical failover process during an outage?** <br>
When the fault is detected by the monitoring system, it initiates a failover workflow that involves making sure the standby has applied all residual WAL files and fully caught up before opening that for read/write. Then DNS is updated with the IP address of the standby before the clients can reconnect to the server with the same endpoint (host name). A new standby is instantiated to keep the configuration in an highly available mode.

* **What is the typical failover time and expected data loss during an outage?** <br>
On a typical case, failover time or the downtime experienced by the application perspective is between 60s-120s. This can be longer in cases where the outage incurred during long running transactions, index creation, or during heavy write activities - as the standby may take longer to complete the recovery process.

Since the replication happens in synchronous mode, no data loss is expected.

* **Do you offer SLA for the failover time?** <br>
For the failover time, we provide guidelines on how long it typically takes for the operation. The official SLA will be provided for the overall uptime when we GA the service. No SLAs are offered during public preview.

* **Does the application automatically connect to the server after the failover?** <br>
No. Applications should have retry mechanism to reconnect to the same endpoint (hostname).

* **How do I test the failover?** <br>
We are working on adding force failover capability to the service. We will update the documentation and also will update this self-help once we enable the capability. For more details, please reach us @ `AskAzureDBforPostgreSQL@service.microsoft.com`.

* **How do I check the replication status?** <br>
On portal, from the overview page of the server shows the Zone redundant high availability status and the server status. You can also check the status and the AZs for primary and standby from the High Availability blade of the server portal. 

From psql, you can run `select * from pg_stat_replication;` which shows the streaming status amongst other details.

* **Can I use the standby replica for read queries?** <br>
Currently, we do not expose standby replica server details and hence you won't be able to perform read queries. However, if you have configured HA in private access (VNET), the standby IP address is exposed and you may be able to perform read queries. 

* **Can I enable or disable HA any any point of time?** <br>

Yes. You can enable or disable zone-redundant HA at any time except when the server is in certain states like stopped, restarting, or already in the process of failing over. 

* **Can I choose the AZ for the standby?** <br>
No. Currently you cannot choose the AZ for the standby. We plan to add that capability in future.

* **When I do point-in-time recovery (PITR), will it automatically configure the restored server in HA?** <br>
No. PITR server is restored as a standalone server. If you want to enable HA, you can do that after the restore is complete.

* **Can I configure HA between private (VNET) and public access?** <br>
No. You can either configure HA within a VNET (spanned across AZs within a region) or public access. 

* **Can I configure HA across regions?** <br>
No. HA is configured within a region, but across availability zones. In future, we are planning to offer read replicas that can be configured across regions for disaster recovery (DR) purposes. We will provide more details when the feature is enabled. 

* **Can I use logical replication with HA configured servers?** <br>
You can configure logical replication with HA. However, after a failover, the logical slot details are not copied over to the standby. Hence, there is currently limited support for this configuration.

## **Recommended steps**
* You can choose the region and the availability zone to deploy your primary database server. A standby replica server is provisioned in a different availability zone with the same configuration as the primary server, including compute tier, compute size, storage size, and network configuration.
* High availability is not supported with burstable compute tier. Please choose General Purpose or Memory Optimized tiers.
* High availability is supported only in regions where multiple zones are available.
* Due to synchronous replication to another availability zone, applications can experience elevated write and commit latency
* Depending on the activity on the primary server at the time of failover, it might take up to two minutes or longer for the failover to complete
* Restarting the primary database server to pick up static parameter changes also restarts the standby replica


## **Recommended Documents**

* [Flexible server - High availability](https://docs.microsoft.com/azure/postgresql/flexible-server/concepts-high-availability)
* [Flexible server - Business continuity](https://docs.microsoft.com/azure/postgresql/flexible-server/concepts-business-continuity)
