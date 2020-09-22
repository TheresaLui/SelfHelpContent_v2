<properties
    pageTitle="Managing firewall rules for Azure Database for MariaDB"
    description="Managing firewall rules for Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="370"
    selfHelpType="generic"
    supportTopicIds="32640122"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7ce043ed-e999-4b4e-ba5e-cfe5388cea80"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Managing firewall rules for Azure Database for MariaDB

Server-level firewall rules are used to manage access to your Azure Database for MariaDB server. You can specify specific IP address or a range of IP addresses. These firewall rules can be managed through the Azure [portal](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-portal), the [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-cli), and our [REST API](https://docs.microsoft.com/rest/api/mariadb/).

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you cannot connect after setting up a firewall rule for your client:

  * Make sure your security credentials are valid in case you are seeing the authentication errors
  * Validate that the firewall on the client allows outbound traffic on the required ports
  * If you client does not have a static IP address, your IP address might not be covered by the firewall rule

* There may be as much as a five-minute delay for changes to the Azure Database for MariaDB server firewall configuration to take effect. Confirm your rule was added and re-try to connect after at least five minutes.

* To set up firewall rules on your client for outbound connection to Azure Database for MariaDB, whitelist the gateway IP for your particular region. For information related to gateway IP addresses, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mariadb/concepts-connectivity-architecture#azure-database-for-mariadb-gateway-ip-addresses).

* If you are having trouble using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az mariadb server firewall-rule** with valid values. Review the [Azure CLI MariaDB firewall rule](https://docs.microsoft.com/cli/azure/mariadb/server/firewall-rule?view=azure-cli-latest) documentation for valid parameters.

* Server's IP appears to be public and you can ping or connect using telnet:

  * Connections to the Azure Database for MariaDB server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mariadb/concepts-connectivity-architecture).

## **Recommended Documents**

* [Managing firewall rules in the portal](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-portal/)<br>
* [Managing firewall rules using CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-cli/)<br>
* [Firewall rule concepts in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules)<br>
* [Azure Database for MariaDB CLI reference documentation](https://docs.microsoft.com/cli/azure/mariadb?view=azure-cli-latest)<br>
* [Azure Database for MariaDB REST API reference documentation](https://docs.microsoft.com/rest/api/mariadb/)
