<properties
    pageTitle="Managing server parameters in Azure Database for MySQL"
    description="Managing server parameters in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="440"
    selfHelpType="generic"
    supportTopicIds="32640070"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2e852f4c-511e-4f71-bb13-b7b13fb05801"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Managing server parameters in Azure Database for MySQL

Azure Database for MySQL allows you to configure parameters at a server level using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters) or the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli). To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal.

> [!NOTE]
> The server parameter `enforce_gtid_consistency` was configured to ON to help with avoiding unexpected issues after enabling GTID in the future. In some cases transaction may violate the GTID consistency and you may experience issues blocking your workload with an error like "ERROR: Statement violates GTID consistency".<br>
If you do not want to enforce GTID, please contact support or our team at AskAzureDBforMySQL@service.microsoft.com with your subscription ID & server name and we will help update the parameter.

## **Recommended Steps**

* To change the **time_zone** parameter, follow the [instructions](https://docs.microsoft.com/azure/mysql/howto-server-parameters#working-with-the-time-zone-parameter) to populate the time zone table
* To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas (ex. `log_bin_trust_function_creators`,`innodb_file_per_table` are locked on both master and replica). Refer to [documentation](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#server-parameters) for the list of parameters that are locked. To update one of the locked parameters on the master server, please delete replica servers, update the parameter value on the master, and recreate replicas.
* Review the [server parameter limitations](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#considerations-and-limitations) for read replica server
* Query Performance Insights, Performance Recommendations do not work for read replica servers. Query Store for read replica servers contains a copy of the master server's data.
* If the server parameter you want to update is not listed in the Azure portal, you can optionally set the parameter at the connection level using **init_connect**. Refer to [setting parameter not listed](https://docs.microsoft.com/azure/mysql/howto-server-parameters#setting-parameters-not-listed)
* If a parameter you'd like to configure is not listed and you want to set at a server level, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/597982-azure-database-for-mysql)
* Server parameters can be updated globally at the server-level, use the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli), [PowerShell](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-powershell), or [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters).
* If there is a change in the server's parameter value from the portal, sometime the client does not see the parameter changed. In such cases client need to reconnect to take param effect after updating param on portal.
* When using read replicas, some server parameters are locked from being updated to prevent data from becoming out of sync and to avoid potential data loss. Refer to [documentation](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#server-parameters) for the list of parameters that are locked.
* If the server is in read-only mode, please either increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#reaching-the-storage-limit) or enable storage **auto-growth**.Review [How to enable storage auto-growth](https://docs.microsoft.com/azure/mysql/howto-auto-grow-storage-portal#enable-storage-auto-grow).

## **Recommended Documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters)<br>
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli)
