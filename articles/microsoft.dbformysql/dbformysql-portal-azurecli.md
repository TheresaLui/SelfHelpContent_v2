<properties
    pageTitle="Design, Development, and APIs for MySQL - CLI"
    description="Design, Development, and APIs for MySQL - CLI"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="310"
    selfHelpType="generic"
    supportTopicIds="32640047"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="0f4e6418-9420-4958-9bf6-013ec38d1206"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Using Azure CLI for Azure Database for MySQL

Azure Database for MySQL has rich support for managing your server in the Azure CLI. Most customers were able to solve the issues with CLI reviewing the recommended steps.

## **Recommended Steps**

* Make sure you are signed-in to the correct using **az login**
* You are using the correct subscription in case you have more than one
* You specify all required parameters for the command you are using. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values
* If you are:

  * Creating server, review [Create an Azure Database for MySQL using CLI](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
  * Setting up firewall rules, review [How-to configure firewall rules using CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli)
  * Trying to restore, review [How-to restore a server using CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
  * Changing server parameters, review [How-to configure server parameters using CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli)
  * Trying to access the server logs, review [How-to access server logs using CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-cli)
  * Setting up replication, review [How-to setup replication using CLI](https://docs.microsoft.com/azure/mysql/howto-read-replicas-cli)
  * Setting up virtual networks, review [How-to setup virtual networks using CLI](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli)
  * Moving a server across resource groups or subscriptions, review [Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)


## **Recommended Documents**

* [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [Azure Database for MySQL CLI sample script collection](https://docs.microsoft.com/azure/mysql/sample-scripts-azure-cli)
