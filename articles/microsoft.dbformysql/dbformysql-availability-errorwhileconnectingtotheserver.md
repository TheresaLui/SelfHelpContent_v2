<properties
  pagetitle="Connection issues to Azure Databases for MySQL&#xD;"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="janeng,bahusse"
  selfhelptype="Generic"
  supporttopicids="32640053"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="996e511f-55ca-4660-80d4-15a2aa76953b"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Connection issues to Azure Databases for MySQL

* **Is the connection failure intermittent?** [Troubleshoot transient errors](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues#troubleshoot-transient-errors)

* **Azure Database for MySQL server has gone away?** [MySQL gone away troubleshooting guide](https://techcommunity.microsoft.com/t5/azure-database-support-blog/azure-database-for-mysql-server-has-gone-away/ba-p/369138)

* **Can connect from a device but can't from another device** This happen due to client side firewall that is blocking outbound connections or private network that is not allowed to connect to the Azure Database for MySQL, Install [psping](https://docs.microsoft.com/sysinternals/downloads/psping) on your client machine to verify connectivity to Azure Database for MySQL, also try connecting from a public network.

* **Access denied for user 'user'@'IP_Address' (using password: YES)** [Error 1045 troubleshooting guide](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1045-28000-access-denied-for-user-usernameip-address-using-password-yes)

* **Client with IP address 'XXX.XX.XXX.X' is not allowed to connect to this MySQL server.** Make sure the IP address is allowed on the [server Firewall rule](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) and that you are using correct username format "your_user@servername" and the right password.

* **ERROR 2013: Lost connection to MySQL server during query**
This is a common error for MySQL databases, try to increase the value of the following parameters to solve this issue: Max_allowed_packet, Connect_timeout, net_write_timeout, net_read_timeout, wait_timeout. Maxing out resource utilization can yield to this error too, please check [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815)

* **The last packet sent successfully to the server was X milliseconds ago. The driver has not received any packets from the server**.
You should consider either expiring and/or testing connection validity before using it in your application, increasing the server configured values for client timeouts, or using the Connector/J connection property 'autoReconnect=true' to avoid this problem.

* **Change username format from your_user@servername or port 3306** Please note that this is the only accepted format to connect to Azure Database for MySQL single server and changing the username format is not possible, port 3306 is the only allowed port and changing it is not possible.

* **Can't connect using SSMS** Consider using MySQL Workbench or mysql native client to connect to Azure Database for MySQL, SSMS is only compatible with Azure SQL Database and can't connect to Azure Database for MySQL.

* **Timeout or dropped connection** Reaching resource limits in terms of CPU, Memory, Number of allowed connections or IOPS is the main reason for timeouts, read [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).

* **Database is in readonly mode** Servers with less than equal to 100 GB provisioned storage are marked read-only if the free storage is less than 5% of the provisioned storage size. [Reaching the storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#reaching-the-storage-limit).

* **SSL issues** [Configure SSL connectivity in your application to securely connect to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-configure-ssl).

* **VNET Issues** [Create and manage Azure Database for MySQL VNet service endpoints and VNet rules](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal).

* **Is the connection failure persistent?** [Troubleshoot persistent errors](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues#troubleshoot-persistent-errors)

    Possible reasons: incorrect firewall configuration, an incorrect connection string, an incorrect VNet configuration, missing permissions for the user that is trying to connect, and others. Work through the recommended steps to ensure you are not hitting a misconfiguration problem. and [Setup alerts when your Azure Database for MySQL server is not accessible](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/get-alerted-when-your-azure-database-for-mysql-server-is-not/ba-p/1996368).

## **Recommended Steps**

### **Intermittent connection errors**
Causes of intermittent connection issues include server restart, high resource utilization on the server, and client timeouts. The following steps could help you resolve the issue:

* Retry the connection
* Check your server metrics to see if any resource is near 100% utilization. High utilization may lead to unavailable resources for a new connection.
* Check your client's timeout settings
* If the issue persists, see persistent connection errors below.

### **Persistent connection errors**

**Note: We are working on changing out gateway certificate used to [connect to the server using SSL](https://docs.microsoft.com/azure/mysql/concepts-ssl-connection-security#ssl-default-settings). Refer to [this article](https://docs.microsoft.com/azure/mysql/concepts-certificate-rotation) to understand the impact and steps to take to avoid connectivity issues.**

If connection issues last for more than a couple minutes, the root cause may be a more persistent issue. Persistent connection issues when connecting to Azure Databases for MySQL can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect virtual network (VNet) configuration, missing permissions for the user that is trying to connect, and other reasons. Work through the recommended steps to ensure you are not hitting a misconfiguration issue.

* Set up firewall rules to be able to connect from your client machine. See how to configure firewall on [Single Server](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) and [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-connect-tls-ssl) to allow your client's IP address.
* If you are using Virtual network, ensure the service endpoints are correctly configured:

	* [How to enable VNET  for Single Server](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)
	* [How to enable VNET  for Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-portal)

* If using Single Server , make sure the user name is in this format 'username@servername' in the connection string. If you are using Flexible Server , make sure user name in connection string does not have '@servername'.
* If you are using a non-admin user for your database, make sure the user has the write permissions. See [how to create non-admin users](https://docs.microsoft.com/azure/mysql/howto-create-users).
* Check if SSL is enabled and update your application to use SSL. Check the documentation for your application type you are using on how to enable SSL.
* Make sure you are using the correct TLS configuration for [Single Server](https://docs.microsoft.com/azure/mysql/howto-tls-configurations) and  [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-connect-tls-ssl)

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)