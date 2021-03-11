<properties
  pagetitle="Client with IP address 'XXX.XX.XXX.X' is not allowed to connect to this MySQL server"
  description="Client with IP address 'XXX.XX.XXX.X' is not allowed to connect to this MySQL server"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788507"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="0ebb58e1-356b-4070-b75f-e73ead0df8e8"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Client with IP address 'XXX.XX.XXX.X' is not allowed to connect to this MySQL server

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

Make sure the IP address is allowed on the [server firewall rule](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) and that you are using the correct username format, your_user@servername, and the right password. For purposes of temporary testing only, set up a firewall rule using 0.0.0.0 as the starting IP address and 255.255.255.255 as the ending IP address. This opens the server to all IP addresses. If this resolves your connectivity issue, remove this rule, and create a firewall rule for an appropriately limited IP address or address range.

**Client firewall configuration**

To ensure that the firewall on your client computer allows connections to your database server:

* Confirm that your network allows outbound connections on port 3306 (this port number cannot be changed). Try to telnet to your server. When using the Single Server deployment mode, confirm that your network/firewall does not block connection to the regional Azure Database for MySQL Gateway IP.
* Test the connection to the MySQL database server by using psping. When using MySQL Single Server deployment mode, ping the FQDN and to verify that it resolves to our Gateway IP correctly. If you’re using the private endpoint, it should resolve to your private IP.
* If you're connecting from an Azure VM (virtual machine), check NSG (network security groups) rules to determine if they block the connection. Also check the route table to see if there is any VPN device that may need to be configured.  
* If you're using VNet rules, ensure that the service endpoints are correctly configured. To find out more and learn about some limitations, see [Use Virtual Network service endpoints and rules for Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-data-access-and-security-vnet).  
* If you're using Private Link and the **Deny public network access** setting is on, you can only connect from the same VNet as the private endpoint, a peered VNet, or via VPN/express route.

## **Recommended documents**

* [Azure Database for MySQL server firewall rules](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)
* [Create and manage Azure Database for MySQL firewall rules by using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal)
