<properties
    pageTitle="Managing firewall rules for Azure Database for PostgreSQL"
    description="Managing firewall rules for Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="230"
    selfHelpType="resource"
    supportTopicIds="32639980"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="5705595d-4b91-4fed-8a03-f71cb0f1dcc5"
/>

# Managing firewall rules for Azure Database for PostgreSQL

Server-level firewall rules are used to manage access to your Azure Database for PostgreSQL server. You can specify specific IP address or a range of IP addresses. These firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/postgresql/).

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you cannot connect after setting up a firewall rule for your client:

  * Make sure your security credentials (username@servername, password) are valid in case you are seeing authentication errors
  * Validate that the firewall on the client allows outbound traffic on the required ports
  * If your client does not have a static IP address, the current IP address might not be covered by the firewall rule

* There may be as much as a five minute delay for changes to the Azure Database for PostgreSQL firewall configuration to take effect. Confirm your rule was added and re-try to connect for at least 5 minutes.

* If you are having trouble using Azure CLI:

  * Make sure you are signed in to the correct Azure account using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az postgres server firewall-rule** with valid values. Review the [Azure CLI PostgreSQL firewall rule](https://docs.microsoft.com/cli/azure/postgres/server/firewall-rule?view=azure-cli-latest) documentation for valid parameters.

## **Recommended Documents**

* [Managing firewall rules in the portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal)<br>
* [Managing firewall rules using CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli)<br>
* [Firewall rule concepts in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules)<br>
* [Azure Database for PostgreSQL CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest)<br>
* [Azure Database for PostgreSQL REST API reference documentation](https://docs.microsoft.com/rest/api/postgresql/)
