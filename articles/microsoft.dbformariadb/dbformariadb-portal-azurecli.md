<properties
    pageTitle="Design, Development, and APIs for MariaDB - CLI"
    description="Design, Development, and APIs for MariaDB - CLI"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="310"
    selfHelpType="generic"
    supportTopicIds="32640114"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="4b87dfd3-880f-45e4-8c17-95d85007095f"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Using Azure CLI for Azure Database for MariaDB

Azure Database for MariaDB has rich support for managing your server in the Azure CLI. Most customers were able to solve the issues with CLI reviewing the recommended steps.

## **Recommended Steps**

* Make sure you are signed-in to the correct using **az login**
* You are using the correct subscription in case you have more than one
* You specify all required parameters for the command you are using Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mariadb?view=azure-cli-latest) for required parameters and valid values.
* If you are:

  * Creating server, review [Create an Azure Database for MariaDB using CLI](https://docs.microsoft.com/azure/mariadb/quickstart-create-mariadb-server-database-using-azure-cli)
  * Setting up firewall rules, review [How-to configure firewall rules using CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-cli)
  * Trying to restore, review [How-to restore a server using CLI](https://docs.microsoft.com/azure/mariadb/howto-restore-server-cli)
  * Changing server parameters, review [How-to configure server parameters using CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-server-parameters-cli)
  * Trying to access the server logs, review [How-to access server logs using CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-server-logs-cli)
  * Setting up replication, review [How-to setup replication using CLI](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli)
  * Setting up virtual networks, review [How-to setup virtual networks using CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-cli)
  * Moving a server across resource groups or subscriptions, review [Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)


## **Recommended Documents**

* [CLI reference documentation](https://docs.microsoft.com/cli/azure/mariadb?view=azure-cli-latest)<br>
* [Azure Database for MariaDB CLI sample script collection](https://docs.microsoft.com/azure/mariadb/sample-scripts-azure-cli)
