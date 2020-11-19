<properties
    pageTitle="Connection issues to Azure Databases for MySQL"
    description="Connection issues to Azure Databases for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32640053"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="996e511f-55ca-4660-80d4-15a2aa76953b"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connection issues to Azure Databases for MySQL

Persistent connection issues when connecting to Azure Databases for MySQL can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect VNet configuration, missing permissions for the user that is trying to connect, and others. Work through the recommended steps to ensure you are not hitting a misconfiguration problem.

## **Recommended Steps**

### **Intermittent connection errors**
Causes of intermittent connection issues include server restart, high resource utilization on the server, and client timeouts. The following steps could help you resolve the issue:

* Retry the connection
* Check your server metrics to see if any resource is near 100% utilization. High utilization may lead to unavailable resources for a new connection.
* Check your client's timeout settings
* If the issue persists, see below

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

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
