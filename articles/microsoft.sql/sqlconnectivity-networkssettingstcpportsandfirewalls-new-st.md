<properties
    pageTitle="How to questions: Network settings, TCP ports and Firewalls"
    description="How to questions: Network settings, TCP ports and Firewalls"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745434"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="F2FFA29C-B6AF-462F-88AA-C1984A034C03"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# How to questions: Network settings, TCP ports and Firewalls

## **Recommended Steps**

### How to questions: Network settings, TCP ports and Firewalls

Before your computer can access an Azure SQL Database, you may need to create a firewall exception on your computer for TCP port 1433.

**Network Settings**: The connectivity settings are accessible from Server > Firewall Rules and Virtual Networks, and configuring at the server level will apply to all SQL Databases associated with the server.

 - TLS Version - Visit [Minimal TLS Version](https://docs.microsoft.com/azure/azure-sql/database/connectivity-settings?WT.mc_id=pid:13491:sid:32745434/#minimal-tls-version) for commands to set the TLS version or if you have further questions or concerns.

 - Connection Policy - Connection policy determines how your clients connect to your SQL Databases. To change connection policies, please visit [Change connection policy](https://docs.microsoft.com/azure/azure-sql/database/connectivity-settings?WT.mc_id=pid:13491:sid:32745434/#change-connection-policy)

- IP Addresses - To connect to your SQL Database, you need to allow the network traffic to and from all the Gateway (IPs) for the region where the DB has been hosted. For more information on gateway IPs and status on new Gateways in specific regions, please visit [Gateway IP addresses](https://docs.microsoft.com/azure/azure-sql/database/connectivity-architecture?WT.mc_id=pid:13491:sid:32745434/#gateway-ip-addresses)

**TCP Ports**: To make connections inside the Azure cloud boundary, you may have to open additional ports as needed. Please follow the instructions in [Ports beyond 1433 for ADO.NET 4.5](https://docs.microsoft.com/azure/azure-sql/database/adonet-v12-develop-direct-route-ports?WT.mc_id=pid:13491:sid:32745434/)

**Firewalls**: Visit [Troubleshoot the database firewall](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure?WT.mc_id=pid:13491:sid:32745434/#troubleshoot-the-database-firewall) for troubleshooting firewall related configuration issues.<br>
