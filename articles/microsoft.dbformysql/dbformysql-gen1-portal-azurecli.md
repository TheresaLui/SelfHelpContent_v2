<properties
    pageTitle="Using Azure CLI for Azure Database for MySQL Single Server"
    description="Using Azure CLI for Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="280"
    selfHelpType="generic"
    supportTopicIds="32747547"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="71125af0-b102-4a08-9a3a-9c7a0f4fc849"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Using Azure CLI for Azure Database for MySQL Single Server

Azure Database for MySQL Single Server can be managed through the Azure CLI. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you may have to poll the status of the operation when using Azure CLI.

## **Recommended Steps**

* Make sure you are signed-in to the correct using **`az login`**
* You are using the correct subscription in case you have more than one
* You specify all required parameters for the command you are using. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values
* Refer to the following links for guidance on specific features:

    | Operation/feature | Flexible server |
    |--|--|
    |Create server|[Quickstart](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)|
    |Firewall rules|[Manage rules](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli)|
    |VNet service endpoints|[Manage VNet service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli)|
    |Private Link|[Manage Private Link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-cli)|
    |Restore|[Perform restore](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)|
    |Replication|[Manage replicas](https://docs.microsoft.com/azure/mysql/howto-read-replicas-cli)|
    |Server parameters|[Configure parameters](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli)|
    |Monitor server|[Configure alerts](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric|
    |Move server across resource groups or subscriptions|[Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)|

## **Recommended Documents**

* [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [Azure Database for MySQL CLI sample script collection](https://docs.microsoft.com/azure/mysql/sample-scripts-azure-cli)
