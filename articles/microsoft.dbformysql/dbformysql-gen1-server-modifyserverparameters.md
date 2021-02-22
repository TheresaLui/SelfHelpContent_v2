<properties
    pageTitle="Managing server parameters in Azure Database for MySQL Single Server"
    description="Managing server parameters in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="440"
    selfHelpType="generic"
    supportTopicIds="32747571"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fb94d0aa-ea44-45cf-be55-803f1c191895"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Managing server parameters in Azure Database for MySQL - Single Server

With Azure Database for MySQL Single Server, you can configure parameters at the server level by using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters) or the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli). To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal.

> **Note:** The server parameter `enforce_gtid_consistency` was configured to ON to help with avoiding unexpected issues after enabling GTID in the future. In some cases transaction may violate the GTID consistency and you may experience issues blocking your workload with an error like "ERROR: Statement violates GTID consistency".<br>
If you do not want to enforce GTID, please contact support or our team at AskAzureDBforMySQL@service.microsoft.com with your subscription ID & server name and we will help update the parameter.

## Fix it yourself

* To update server parameters globally at the server-level, use the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli), [PowerShell](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-powershell), or [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters). If you change the value of a server parameter using the portal, occasionally the client does not recognize the changed parameter. In this case, reconnect the client to have the parameter take effect.
* To update a server parameter not listed in the Azure portal, set the parameter at the connection level using `init_connect`. For more information, see [setting parameter not listed](https://docs.microsoft.com/azure/mysql/howto-server-parameters#setting-parameters-not-listed). If you need to update a server parameter that is not listed in the Azure portal at the server level, create a new request or vote for an existing request in our [feedback forum](https://feedback.azure.com/forums/597982-azure-database-for-mysql) to let us know.
* When using read replicas, some server parameters are locked from being updated to prevent data from becoming out of sync and to avoid potential data loss or corruption. For a list of parameters that are locked, see [Server parameters](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#server-parameters) for the list of parameters that are locked. To update any locked parameter on the master server, delete all replica servers, update the parameter value on the master, and then recreate the replicas.Also review the [Considerations and parameter limitations](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#considerations-and-limitations) for a read replica server. Note that Query Performance Insights and Performance Recommendations don’t work on read replica servers. Query Store for read replica servers contains a copy of the master server's data.
* For more information about the `time_zone` parameter, see [time_zone](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#time_zone). To populate the time zone table, see [Working with the time zone parameter](https://docs.microsoft.com/azure/mysql/howto-server-parameters#working-with-the-time-zone-parameter).
* If the server is in read-only mode, either use the portal to increase the storage size as described in [Reaching the storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#reaching-the-storage-limit) or enable storage **auto-growth**. For more information, see [How to enable storage auto-growth](https://docs.microsoft.com/azure/mysql/howto-auto-grow-storage-portal#enable-storage-auto-grow).

## Tips

Make sure to consider the following points.

* Connections to an Azure Database for MySQL server are established through a gateway responsible for routing incoming connections to the physical location of the server in our clusters. A client attempting to connect will first reach the gateway service, which is hosted on group of stateless compute nodes sitting behind an IP address. As part of ongoing service maintenance, the IP address of this gateway service changes, so avoid hard coding the gateway IP address in your application’s connection string. Instead, use the fully qualified domain name (FQDN) of your server in the format `.mysql.database.azure.com`, in the connection string. For more information, see [Azure Database for MySQL gateway IP addresses](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture#azure-database-for-mysql-gateway-ip-addresses).

## **Recommended documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters)
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli)
