<properties
    pageTitle="Managing firewall rules for Azure Database for MySQL"
    description="Managing firewall rules for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="20"
    selfHelpType="resource"
    supportTopicIds="32640056"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="30b8bd3a-7cc7-4535-a008-910a22a6318a"
/>

# Managing firewall rules for Azure Database for MySQL

Server-level firewall rules are used to manage access to your Azure Database for MySQL Server. You can specify specific IP address or a range of IP addresses. These Firewall rules can be managed through the Azure [portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/mysql/).

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you cannot connect after setting up a firewall rule for your client:

  * Make sure your security credentials are valid in case you are seeing the authentication errors
  * Validate that the firewall on the client allows outbound traffic on the required ports
  * If you client does not have a static IP address, your IP address might not be covered by the firewall rule

* There may be as much as a five-minute delay for changes to the Azure Database for MySQL Server firewall configuration to take effect. Confirm your rule was added and re-try to connect for at least 5 minutes.
* If you are having trouble using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az mysql server firewall-rule** with valid values. Review the [Azure CLI MySQL firewall rule](https://docs.microsoft.com/cli/azure/mysql/server/firewall-rule?view=azure-cli-latest) documentation for valid parameters.

## **Recommended Documents**

* [Managing firewall rules in the portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal)<br>
* [Managing firewall rules using CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli)<br>
* [Firewall rule concepts in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)<br>
* [Azure Database for MySQL CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [Azure Database for MySQL REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/)
