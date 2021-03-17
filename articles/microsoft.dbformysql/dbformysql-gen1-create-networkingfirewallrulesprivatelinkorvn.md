<properties
    pageTitle="Networking in Azure Databases for MySQL - Single Server"
    description="Networking in Azure Databases for MySQL - Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32747574"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f1620891-8d93-42fb-a041-115572400ed2"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Networking in Azure Databases for MySQL - Single Server

There are three networking option to access your Azure Database for MySQL Single Server.

* Private Link
* VNet Service endpoints
* Firewall rules

Please refer to recommended steps for respective section for resolving common issues.

## **Recommended Steps**

### Private Link

Private Link allows you to connect to various PaaS services in Azure via a private endpoint. Azure Private Link essentially brings Azure services inside your private Virtual Network (VNet). The PaaS resources can be accessed using the private IP address just like any other resource in the VNet.

* If you are using Private Link ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* If you are using a Basic tier server, note that [Private Link](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link) is not supported

### VNet Service endpoints

Virtual network rules are firewall rules that control whether your Azure Database for MySQL Single Server accepts connections from a particular subnet in a virtual network. Virtual network rules can be configured using the Azure portal and Azure CLI.

* Ensure that the Azure Database for MySQL Single Server uses the General Purpose or Memory optimized tier. The Basic tier does not support VNet service endpoints.
* If you are using multiple subscriptions make sure that both the subscription has the Microsoft.Sql resource provider registered. For more information refer [resource-manager-registration](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-supported-services) how-to
* If you are using multiple subscriptions all of them must be in the same Azure Active Directory tenant.
* Ensure that you have turned on [VNet service endpoints](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview) for your VNet
* To familiarize yourself with using ARM templates to create virtual network rules in Azure Database for MySQL Single Server, refer to [Deploy multiple properties of a server including Firewall rules, Virtual Network rules, server parameters or databases](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithMultipleServerProperties) ARM template.

### Firewall rules

Server-level firewall rules are used to manage access to your Azure Database for MySQL Single Server. You can specify specific IP address or a range of IP addresses. These Firewall rules can be managed through the Azure [portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/mysql/).

* If you cannot connect after setting up a firewall rule for your client:

  * Make sure your security credentials are valid in case you are seeing the authentication errors
  * Validate that the firewall on the client allows outbound traffic on the required ports
  * If you client does not have a static IP address, your IP address might not be covered by the firewall rule

* There may be as much as a five-minute delay for changes to the Azure Database for MySQL Single Server firewall configuration to take effect. Confirm your rule was added and re-try to connect for at least 5 minutes.

* To set up firewall rules on your client for outbound connection to Azure Database for MySQL Single Server, whitelist the gateway IP for your particular region. For information related to gateway IP addresses, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture#azure-database-for-mysql-gateway-ip-addresses).

* Specify all required parameters in **az mysql server firewall-rule** with valid values. Review the [Azure CLI MySQL firewall rule](https://docs.microsoft.com/cli/azure/mysql/server/firewall-rule?view=azure-cli-latest) documentation for valid parameters.

* If you are deploying or updating multiple server attributes which includes firewall rules, Virtual Network rules, server parameters or databases for a given server, make sure you are deploying these serially, in any order. By default, ARM deploys resources in parallel and a deployment may fail if configured in parallel. Familiarize yourself with [Sample ARM templates](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithMultipleServerProperties).

## **Recommended Documents**

* [Use Virtual Network service endpoints and rules for Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/concepts-data-access-and-security-vnet/)
* [Managing firewall rules in the portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal)<br>
* [Firewall rule concepts in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)<br>
* [Azure Database for MySQL Single Server CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [Azure Database for MySQL Single Server REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/)