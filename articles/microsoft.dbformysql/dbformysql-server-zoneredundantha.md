<properties
    pageTitle="Zone redundancy for Azure Database for MySQL"
    description="Zone redundancy for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="Bashar-MSFT"
    ms.author="jtoland"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32788529"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="34e0669a-3ae8-429e-aee6-98750f6c9548"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Zone redundant high availability for Azure Database for MySQL

With Azure Database for MySQL Flexible Server, you can provision MySQL servers so that if the availability zone the database server is running in fails, the service simply reverts to using a secondary server running in a different zone in the same region. This happens without any manual intervention.

The process of failure detection, DNS switching, and failover to the secondary server typically occurs within 60 - 120 seconds. Setting up the service this way provides the 99.99% service level agreement (SLA). It's important to note, however, that zone redundant high availability requires running two similar servers, so the total cost is double that of running only a primary server.

**IMPORTANT**: This functionality is only supported for servers running Azure Database for MySQL Flexible Server.

## Quick tips

* Setting up zone redundant high availability after creating a server isn't currently supported. Setup must occur as part of server creation.
* Enabling zone redundant high availability requires using the **general purpose** or **memory optimized** pricing tier
* In region read replica can't be enabled for zone redundant high available servers. In addition, zone redundant high availability for a replica server can't be enabled.
* Zone redundant available servers can't be Stopped/Started. In addition, the hot standby running as part of a zone redundant available setup is not available for read purposes.

## **Recommended documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-high-availability)
