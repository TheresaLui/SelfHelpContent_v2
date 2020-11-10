<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32639977, 32780963"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="14dc0ce8-a36f-4736-bd56-48f33e04eddd"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Error while connecting to server

## **Recommended Steps**

### **Intermittent connection errors**

Causes of intermittent connection issues include server restart, high resource utilization on the server, and client timeouts. The following steps could help you resolve the issue:

* Retry the connection to see if the problem persists
* When you see **An existing connection was forcibly closed by the remote host**, that indicates your client closed the connection to the Postgres server. Check your client timeout and idle connection settings. [Learn more about this error](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/troubleshoot-postgresql-an-existing-connection-was-forcibly/ba-p/925164)
* There may be a planned maintenance activity going on your database server. Check your Resource Health for the current status. You may also want to [setup planned maintenance notifications](https://docs.microsoft.com/azure/postgresql/concepts-monitoring#planned-maintenance-notification) to get notified of any planned activities.
* Check your server metrics to see if any resource is near **100% utilization**. Review how many connections your server has and how many more you are attempting. High utilization may lead to unavailable resources for a new connection.
* Check the [connection limit for your server's pricing tier](https://docs.microsoft.com/azure/postgresql/concepts-limits)


### **Persistent connection errors**

If connection issues last for more than a couple minutes, the root cause may be a more persistent issue. 

* The error **pg_hba.conf entry for host 'xxxx', user 'xxxx', database 'pxxxx', SSL...** indicates that a firewall rule is needed. [Set up firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules) to allow your client's IP address
* Confirm that your network allows outbound connections on port 5432 and to the regional Azure Database for PostgreSQL [Gateway IP](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
* If you see an error related to **GSS**, you are likely using a newer client/driver version which Azure Postgres Single Server does not yet fully support. This error is known to affect [JDBC driver versions 42.2.15 and 42.2.16](https://github.com/pgjdbc/pgjdbc/issues/1868).
   - We plan to complete the update by the end of November. Consider using a working driver version in the meantime.
   - Or, consider disabling the request of GSSAPI.  Use a connection parameter like `gssEncMode=disable`.
* If you are using VNets, ensure that the [service endpoints](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal) are correctly configured
* If you see the error 'Server is not configured to allow **IPv6** connections' on a Basic tier server, note that the Basic tier does not support VNet service endpoints. You have to remove the endpoint Microsoft.Sql from the subnet attempting to connect to the Basic tier server.
* Make sure the user you are connecting with has the appropriate permissions
* Confirm that the username you are passing ends with the correct server name/hostname field (usernames need to be passed as `username@servername`)
* Follow [connection recommendations](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries) on computers hosting your client programs
* Make sure you are using the correct [SSL configuration](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security)
* As a part of our maintenance activity, we are working on changing out gateway certificate used to [connect to the server using SSL](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security). Refer to the steps to mitigate the issue in [this article](https://docs.microsoft.com/azure/postgresql/concepts-certificate-rotation)
* Make sure you are using the correct [TLS configuration](https://docs.microsoft.com/azure/postgresql/howto-tls-configurations)


## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
* [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
* [Understanding the connectivity architecture for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
