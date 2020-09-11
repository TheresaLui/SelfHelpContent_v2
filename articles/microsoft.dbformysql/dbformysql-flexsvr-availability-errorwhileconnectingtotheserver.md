<properties
    pageTitle="Connection issues to Azure Database for MySQL Flexible Server"
    description="Connection issues to Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="rojone"
    ms.author="RohanYJones"
    displayOrder="10"
    selfHelpType="generic"
    supportTopicIds="32747611"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9e8c88bf-2874-490b-82ec-d5e9c03ca38c"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connection issues to Azure Database for MySQL Flexible Server

Persistent connection issues when connecting to Azure Database for MySQL Flexible Server can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect VNet configuration, missing permissions for the user that is trying to connect, and others. Work through the recommended steps to ensure you are not hitting a misconfiguration problem.

## **Recommended Steps**

### **Intermittent connection errors**
Causes of intermittent connection issues include server restart, high resource utilization on the server, and client timeouts. The following steps could help you resolve the issue:

* Retry the connection
* Check your server metrics to see if any resource is near 100% utilization. High utilization may lead to unavailable resources for a new connection.
* Check your client's timeout settings
* If the issue persists, see below

### **Persistent connection errors**

If connection issues last for more than a couple minutes, the root cause may be a more persistent issue. Persistent connection issues when connecting to Azure Database for MySQL Flexible Server can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect virtual network (VNet) configuration, missing permissions for the user that is trying to connect, and other reasons. Work through the recommended steps to ensure you are not hitting a misconfiguration issue.

* [Set up firewall rules in Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-networking#public-access-allowed-ip-addresses) to allow your client's IP address.
* If you are using Private access (VNet Integration), ensure the correct configuration of the [virtual network](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-networking#private-access-vnet-integration).
* Make sure you are using the correct [TLS/SSL configuration](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-connect-tls-ssl)
* Make sure the user you are using has the appropriate permissions

## **Recommended Documents**

* [Configure Private access (VNet Integration) for Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-portal)<br>
* [Configure firewall rules for Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal)
* [Manage TLS/SSL for Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-connect-tls-ssl)