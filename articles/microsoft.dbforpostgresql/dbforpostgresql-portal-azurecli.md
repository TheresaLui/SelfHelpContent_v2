<properties
    pageTitle="Design, Development, and APIs for PostgreSQL - CLI"
    description="Design, Development, and APIs for PostgreSQL - CLI"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="350"
    selfHelpType="generic"
    supportTopicIds="32639969"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ccbe95b1-927f-4e7b-a108-d15114886d8f"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Using Azure CLI for Azure Database for PostgreSQL

Azure Database for PostgreSQL supports managing your server using the Azure CLI. Most customers were able to solve the issues with CLI reviewing the recommended steps.

## **Recommended Steps**

* Make sure you are signed-in to the correct account using **az login**
* You are using the correct subscription in case you have more than one
* You specify all required parameters for the command you are using. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest) for required parameters and valid values.
* If you are:

  * creating server, review [Create an Azure Database for PostgreSQL using CLI](https://docs.microsoft.com/azure/postgresql/quickstart-create-server-database-azure-cli)
  * setting up firewall rules, review [How-to configure firewall rules using CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli)
  * trying to restore, review [How-to restore a server using CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)
  * changing server parameters, review [How-to configure server parameters using CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-cli)
  * trying to access the server logs, review [How-to access server logs using CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-logs-using-cli)
  * setting up replication, review [How-to setup replication using CLI](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)
  * setting up virtual networks, review [How-to setup virtual networks using CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli)
  * moving a server across resource groups or subscriptions, review [Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)

## **Recommended Documents**

* [CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest)<br>
* [Azure Database for PostgreSQL CLI sample script collection](https://docs.microsoft.com/azure/postgresql/sample-scripts-azure-cli)
