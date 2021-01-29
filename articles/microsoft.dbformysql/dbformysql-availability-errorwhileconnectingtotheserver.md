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

Resolve most connection issues to Azure databases for MySQL using the following questions and recommended steps.

## Common questions

* **Is the connection failure intermittent?**<br>
[Troubleshoot transient errors](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues#troubleshoot-transient-errors)

* **Azure Database for MySQL server has gone away?**<br>
See [MySQL gone away troubleshooting guide](https://techcommunity.microsoft.com/t5/azure-database-support-blog/azure-database-for-mysql-server-has-gone-away/ba-p/369138)

* **I can connect from one device, but can't from another device** <br>
This happens because the client-side firewall is blocking outbound connections, or the private network is not allowed to connect to the Azure Database for MySQL. Install [psping](https://docs.microsoft.com/sysinternals/downloads/psping) on your client machine to verify connectivity to Azure Database for MySQL. Also, try connecting from a public network.

* **Error: Access denied for user '*user'@'IP_Address*' (using password: YES)** <br>
See [Error 1045 troubleshooting guide](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1045-28000-access-denied-for-user-usernameip-address-using-password-yes)

* **Error: Client with IP address '*nnn.nn.nnn.n*' is not allowed to connect to this MySQL server.** <br>
Make sure that the IP address is allowed on the [server Firewall rule](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) and that you are using correct username format "your_user@servername" and the right password.

* **Error 2013: Lost connection to MySQL server during query**<br>
This is a common error for MySQL databases. Try to increase the value of the following parameters to solve this issue: `Max_allowed_packet`, `Connect_timeout`, `net_write_timeout`, `net_read_timeout`, `wait_timeout`. Maxing out resource utilization can yield to this error too. Review [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).

* **The last packet sent successfully to the server was *nn* milliseconds ago. The driver has not received any packets from the server**.<br>
You should consider either expiring or testing the connection validity before using it in your application. Increase the server configured values for client timeouts, or use the Connector/J connection property `autoReconnect=true` to avoid this problem.

* **Change username format from your_user@servername or port 3306** <br>
This is the only accepted format to connect to Azure Database for MySQL single server. Changing the username format or port number is not possible. Port 3306 is the only allowed port.

* **Can't connect using SSMS** <br>
Consider using MySQL Workbench or mysql native client to connect to Azure Database for MySQL. SSMS is only compatible with Azure SQL Database and can't connect to Azure Database for MySQL.

* **Timeout or dropped connection** <br>
Reaching resource limits in terms of CPU, Memory, Number of allowed connections or IOPS is the main reason for timeouts. For more information, read [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).

* **Database is in read-only mode**<br>
Servers with less than equal to 100 GB provisioned storage are marked read-only if the free storage is less than 5% of the provisioned storage size. [Reaching the storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#reaching-the-storage-limit).

* **SSL issues**<br>
[Configure SSL connectivity in your application to securely connect to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-configure-ssl).

* **VNET Issues**<br>
[Create and manage Azure Database for MySQL VNet service endpoints and VNet rules](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal).

* **Is the connection failure persistent?**<br>
[Troubleshoot persistent errors](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues#troubleshoot-persistent-errors)

   Possible reasons include: incorrect firewall configuration, an incorrect connection string, an incorrect VNet configuration, missing permissions for the user that is trying to connect, and others. Work through the recommended steps to ensure you are not hitting a misconfiguration problem. [Setup alerts when your Azure Database for MySQL server is not accessible](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/get-alerted-when-your-azure-database-for-mysql-server-is-not/ba-p/1996368).

## **Recommended Steps**

### **Intermittent connection errors**
Causes of intermittent connection issues include server restart, high resource utilization on the server, and client timeouts. The following steps can help you resolve the issue:

* Retry the connection
* Check your server metrics to see if any resource is near 100% utilization. High utilization may lead to unavailable resources for a new connection.
* Check your client's timeout settings
* If the issue persists, see persistent connection errors below.

### **Persistent connection errors**

**Note:** We are working on changing out the gateway certificate used to [connect to the server using SSL](https://docs.microsoft.com/azure/mysql/concepts-ssl-connection-security#ssl-default-settings). Refer to [this article](https://docs.microsoft.com/azure/mysql/concepts-certificate-rotation) to understand the impact and steps to take to avoid connectivity issues.

If connection issues last for more than a couple of minutes, the root cause may be a more persistent issue. Persistent connection issues when connecting to Azure Databases for MySQL can occur because of an incorrect firewall configuration, an incorrect connection string, an incorrect virtual network (VNet) configuration, missing permissions for the user that is trying to connect, and other reasons. Work through the recommended steps to ensure you are not hitting a misconfiguration issue.

* Set up firewall rules to be able to connect from your client machine. See how to configure firewall on [Single Server](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) and [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-connect-tls-ssl) to allow your client's IP address.
* If you use Virtual network, ensure the service endpoints are correctly configured:

	* [How to enable VNET  for Single Server](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)
	* [How to enable VNET  for Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-portal)

* If you use Single Server, make sure that the user name is in this format `username@servername` in the connection string. If you use Flexible Server, make sure that the user name in the connection string does not have `@servername`.
* If you use a non-admin user for your database, make sure that the user has the necessary write permissions. See [how to create non-admin users](https://docs.microsoft.com/azure/mysql/howto-create-users).
* Check if SSL is enabled and update your application to use SSL. Check the documentation for the application type you are using on how to enable SSL.
* Make sure that you are using the correct TLS configuration for [Single Server](https://docs.microsoft.com/azure/mysql/howto-tls-configurations) and [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-connect-tls-ssl).

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
