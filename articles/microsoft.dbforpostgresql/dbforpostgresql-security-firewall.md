<properties
    pageTitle="Managing firewall rules for Azure Database for PostgreSQL"
    description="Managing firewall rules for Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="460"
    selfHelpType="generic"
    supportTopicIds="32639981, 32780946"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3b2cdd35-8f48-40b3-88de-ea7c22c0bdb7"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing firewall rules for Azure Database for PostgreSQL

Server-level firewall rules are used to manage access to your Azure Database for PostgreSQL server. You can specify specific IP address or a range of IP addresses. These firewall rules can be managed through the Azure [portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/postgresql/).

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you cannot connect after setting up a firewall rule for your client:

  * Make sure your security credentials are valid in case you are seeing the authentication errors
  * Validate that the firewall on the client allows outbound traffic on the required port (5432) and [IPs](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture). 
  * If you client does not have a static IP address, your IP address might not be covered by the firewall rule

* There may be as much as a five-minute delay for changes to the Azure Database for PostgreSQL server firewall configuration to take effect. Confirm your rule was added and re-try to connect after at least five minutes.

* If you are having trouble using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az postgres server firewall-rule** with valid values. Review the [Azure CLI PostgreSQL firewall rule](https://docs.microsoft.com/cli/azure/postgres/server/firewall-rule?view=azure-cli-latest) documentation for valid parameters.

* Server's IP appears to be public and you can ping or connect using telnet:

  * Connections to the Azure Database for PostgreSQL server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules.

## **Recommended Documents**

* [Managing firewall rules in the portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal)<br>
* [Managing firewall rules using CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli)<br>
* [Firewall rule concepts in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules)<br>
* [Azure Database for PostgreSQL CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest)<br>
* [Azure Database for PostgreSQL REST API reference documentation](https://docs.microsoft.com/rest/api/postgresql/)
