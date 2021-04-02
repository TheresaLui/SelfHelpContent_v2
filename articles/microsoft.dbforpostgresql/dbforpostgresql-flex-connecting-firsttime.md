<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32789522"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3b3e6dc2-6fd0-4272-8907-45faacb55a5a"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **Error while connecting to the PostgreSQL Flexible Server for the first time**
## **Recommended Steps**

### **Check connection string and password**

- Before you connect a user with an account, make sure they have the appropriate permission
- Make sure the password is correct in all connections. If you've enabled connection throttling server parameter in the portal, the database service will temporarily throttle connections per IP if there are too many invalid password login failures.

### **Check if Security Rules are set correctly**


- Make sure to use the correct [SSL configuration](https://docs.microsoft.com/azure/postgresql/flexible-server/concepts-networking)
- Make sure to use the correct [TLS configuration](https://docs.microsoft.com/azure/postgresql/howto-tls-configurations?WT.mc_id=Portal-Microsoft_Azure_Support)

### **Check firewall rules**
Check the firewall rules in the portal. The error "pg_hba.conf entry for host 'xxxx', user 'xxxx', database 'pxxxx', SSL.." indicates that a firewall rule is needed. Set up [firewall rules](https://docs.microsoft.com/azure/postgresql/flexible-server/how-to-manage-firewall-portal) to allow your client's IP address.
- You can either specify a single IP address or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/postgresql/flexible-server/how-to-manage-firewall-cli), and our [REST API](https://docs.microsoft.com/rest/api/postgresql/).
- If you are trying to connect to your server from an Azure PaaS service that doesn't have a static IP and doesn't support virtual networks, you can turn on [Allow access to Azure services](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules#connecting-from-azure). Turning this on opens the firewall to all Azure IPs.
-  If the server's IP appears to be public and you can ping or connect using telnet, connections to the Azure Database for PostgreSQL server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture).

### **Check if client configuration is set correctly**

- You can simply test the connection from Azure CLI in the portal and see if you can connect. This test can help narrow down if the database is having an availability issue or a client network issue.
- Ping the FQDN and see if it resolves to our [Gateway IP](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture?WT.mc_id=Portal-Microsoft_Azure_Support) correctly. If you're using the private endpoint, it should resolve to your private IP for the private endpoint.
- Confirm that your network allows outbound connections on port 5432. You can try to telnet to your server. Confirm your network/firewall does not block connection to the regional Azure Database for PostgreSQL Gateway IP.
- If you're connecting within Azure VM (virtual machines), check NSG (network security groups) rules to see if it blocks the connection. Also check the route table and see if there is any VPN device which may need to be configured.
- If you're using VNET rules, ensure that the [service endpoints](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal?WT.mc_id=Portal-Microsoft_Azure_Support) are correctly configured.
- If you're using basic tier and see the error "Server is not configured to allow IPv6 connections", note that the Basic tier does not support VNet service endpoints. You must remove the endpoint Microsoft.Sql from the subnet attempting to connect to the Basic tier server.

### **Check if you are using the right connection drivers?**

- Check out this supported [client library](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries) list.
- If you see an error related to GSS, you are likely using a newer client/driver version which Azure PostgreSQL Single Server does not yet fully support. This error is known to affect [JDBC driver versions 42.2.15 and 42.2.16](https://github.com/pgjdbc/pgjdbc/issues/1868).  Consider using a later driver version. Or, consider disabling the request of GSSAPI. Use a connection parameter like `gssEncMode=disable`.


## **Recommended Documents**

- [Quickstart: Connect and query with Azure CLI with Azure Database for PostgreSQL - Flexible Server](https://docs.microsoft.com/azure/postgresql/flexible-server/connect-azure-cli)
