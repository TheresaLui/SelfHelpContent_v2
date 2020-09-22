<properties
    pageTitle="Zone redundancy for Azure Database for MySQL Flexible Server"
    description="Zone redundancy for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32747644"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="902e480e-183c-4a60-bf0e-17ef87455a75"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Zone redundant high availability for Azure Database for MySQL Flexible Server

Azure Database for MySQL Flexible server lets you provision MySQL servers in a zone redundant setup where we have a hot standby provisioned along with the primary server. In case of a failure of the primary zone itself the application will automatically failover to the hot standby running in the secondary zone without any manual intervention. This process of failure detection, DNS switching and the failover to the secondary servers is typically done between 60 - 120 seconds. This setup of running the server gives the 99.99% SLA. One critical thing to note is that the zone redundant high availability runs 2 similar server and therefore is twice the price of the primary server.

## **Recommended Steps**

1.  If you are trying to setup zone redundant high availability post server create, you will not be able to set it up since we currently do not support post server create setup of zone redundant high availability.
2.  If you want to enable zone redundant high availability, you will need to use **general purpose** or **memory optimized** pricing tier.
3.  You cannot enable in region read replica for the zone redundant high available servers. Also, you cannot enable zone redundant high availability for a replica server.
4.  You cannot Stop/Start a zone redundant available servers. Also, the hot standby running in case of a zone redundant available setup is not available for read purposes.

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-high-availability)
