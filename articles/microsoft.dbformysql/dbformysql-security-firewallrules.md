<properties
    pageTitle="Managing firewall rules for Azure Database for MySQL"
    description="Managing firewall rules for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="410"
    selfHelpType="generic"
    supportTopicIds="32640057"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e1475999-0623-4331-ab68-b829a4cd1214"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Managing firewall rules for Azure Database for MySQL

Server-level firewall rules are used to manage access to your Azure Database for MySQL server. You can specify specific IP address or a range of IP addresses. These firewall rules can be managed through the Azure [portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/mysql/).

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you cannot connect after setting up a firewall rule for your client:

  * Make sure your security credentials are valid in case you are seeing the authentication errors
  * Validate that the firewall on the client allows outbound traffic on the required ports and the [required IP addresses](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture)
  * If your client does not have a static IP address, you might have to open the firewall to a range of addresses or update the firewall whenever your client address changes

* There may be as much as a five-minute delay for changes to the Azure Database for MySQL server firewall configuration to take effect. Confirm your rule was added and re-try to connect after at least five minutes.

* To set up firewall rules on your client for outbound connection to Azure Database for MySQL, whitelist the gateway IP for your particular region. For information related to gateway IP addresses, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture#azure-database-for-mysql-gateway-ip-addresses).

* If you are having trouble using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az mysql server firewall-rule** with valid values. Review the [Azure CLI MySQL firewall rule](https://docs.microsoft.com/cli/azure/mysql/server/firewall-rule?view=azure-cli-latest) documentation for valid parameters.

* Server's IP appears to be public and you can ping or connect using telnet:

  * Connections to the Azure Database for MySQL server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture).

## **Recommended Documents**

* [Managing firewall rules in the portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal)<br>
* [Managing firewall rules using CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli)<br>
* [Firewall rule concepts in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)<br>
* [Azure Database for MySQL CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [Azure Database for MySQL REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/)
