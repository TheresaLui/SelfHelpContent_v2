<properties
    pageTitle="Zone redundancy for Azure Database for MySQL"
    description="Zone redundancy for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32747991"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="52b516fd-3e57-4ee9-a72a-04160af4a104"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Zone redundant high availability for Azure Database for MySQL

Azure Database for MySQL lets you provision MySQL servers in a manner that in case of the failure of the availability zone in which database server is running, we simply failover to the secondary server running in a different zone within the same region. All this happens without any manual intervention. This process of failure detection, DNS switching and the failover to the secondary servers is typically done between 60 - 120 seconds. This setup of running the server gives the 99.99% SLA. One critical thing to note is that the zone redundant high availability runs 2 similar server and therefore is twice the price of the primary server.

**NOTE**: **This functionality is only supported in Azure Database for MySQL Flexible Servers.**

## **Recommended Steps**

1.  If you are trying to setup zone redundant high availability post server create, you will not be able to set it up since we currently do not support post server create setup of zone redundant high availability
2.  If you want to enable zone redundant high availability, you will need to use **general purpose** or **memory optimized** pricing tier
3.  You cannot enable in region read replica for the zone redundant high available servers. Also, you cannot enable zone redundant high availability for a replica server.
4.  You cannot Stop/Start a zone redundant available servers. Also, the hot standby running in case of a zone redundant available setup is not available for read purposes.

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-high-availability)
