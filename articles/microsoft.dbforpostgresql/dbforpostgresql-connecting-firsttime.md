<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32788702,32789528"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5d696e46-52a8-46cd-a892-eae71f155e89"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **Error while connecting to the PostgreSQL Server for the first time**

Follow these steps to resolve errors when you connect to the Azure PostgreSQL Server for the first time.

## **Recommended Steps**

### **Check connection string and password**

- Make sure that the user you're connecting with an account has the appropriate permission
- Confirm that you're passing a user name that ends with the correct server name/hostname field. Usernames need to be passed as username@servername.
- Make sure the password is correct in all connections. If you've enabled connection throttling server parameter in the portal, the database service will temporarily throttle connections per IP if there are too many invalid password login failures.

### **Check if aecurity rules are set correctly**

- Make sure that you use the correct [SSL configuration](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security?WT.mc_id=Portal-Microsoft_Azure_Support) and choose the right certificate
- As part of our maintenance activity, we are working on changing out the gateway certificate used to connect to the server [using SSL](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security?WT.mc_id=Portal-Microsoft_Azure_Support). Use the steps in this article to mitigate the issue.
- Make sure that you use the correct [TLS configuration](https://docs.microsoft.com/azure/postgresql/howto-tls-configurations?WT.mc_id=Portal-Microsoft_Azure_Support)

### **Check firewall rules**

Check the firewall rules in the portal. The error "pg_hba.conf entry for host 'xxxx', user 'xxxx', database 'pxxxx', SSL.." indicates that a firewall rule is needed. Set up [firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules?WT.mc_id=Portal-Microsoft_Azure_Support) to allow your client's IP address.
- You can either specify a single IP address or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/postgresql/).
- If you're using a virtual network (VNet), ensure that the service endpoints are correctly configured for the Postgres server and the client. This can be done using the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal) or the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli/).
- If you're using Private Link, ensure that the configuration of the [Private link](https://docs.microsoft.com/azure/postgresql/howto-configure-privatelink-portal) is correct
- If you're using a Basic tier server, note that VNet service endpoints and [Private Link](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-private-link) are not supported
- If you're trying to connect to your server from an Azure PaaS service that doesn't have a static IP and doesn't support virtual networks, you can turn on [Allow access to Azure services](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules#connecting-from-azure). Turning this on opens the firewall to all Azure IPs.
-  If the server's IP appears to be public and you can ping or connect using telnet, connections to the Azure Database for PostgreSQL server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture).

### **Check if client configuration is set correctly**

- You can simply test the connection from Azure CLI in the portal and see if you can connect. This test can help narrow down if the database is having an availability issue or a client network issue.
- Ping the FQDN and see if it resolves to our [Gateway IP](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture?WT.mc_id=Portal-Microsoft_Azure_Support) correctly. If you're using the private endpoint, it should resolve to your private IP for the private endpoint.
- Confirm that your network allows outbound connections on port 5432. You can try to telnet to your server. Confirm your network/firewall does not block connection to the regional Azure Database for PostgreSQL Gateway IP.
- If you're connecting within Azure VM (virtual machines), check NSG (network security groups) rules to see if it blocks the connection. Also check the route table and see if there is any VPN device which may need to be configured.
- If you're using VNet rules, ensure that the [service endpoints](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal?WT.mc_id=Portal-Microsoft_Azure_Support) are correctly configured
- If you're using basic tier and see the error "Server is not configured to allow IPv6 connections," note that the Basic tier does not support VNet service endpoints. You must remove the endpoint Microsoft.Sql from the subnet attempting to connect to the Basic tier server.

### **Check if you are using the right connection drivers**

- See this [supported client library](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries) list.
- If you see an error related to GSS, you are likely using a newer client/driver version which Azure PostgreSQL Single Server does not yet fully support. This error is known to affect [JDBC driver versions 42.2.15 and 42.2.16](https://github.com/pgjdbc/pgjdbc/issues/1868).  Consider using a later driver version. Or, consider disabling the request of GSSAPI. Use a connection parameter like `gssEncMode=disable`.


## **Recommended Documents**

- [Troubleshoot common connectivity issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
- [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
- [Understanding the connectivity architecture for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
