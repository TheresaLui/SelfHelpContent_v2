<properties
    pageTitle="Using Azure CLI for Azure Database for MySQL"
    description="Using Azure CLI for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
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

Azure Database for MySQL offers two deployment types - single server and flexible server. Both types of servers can be managed through the Azure CLI. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you may have to poll the status of the operation when using Azure CLI or REST APIs.

## **Recommended Steps**

* Make sure you are signed-in to the correct using **`az login`**
* You are using the correct subscription in case you have more than one
* You specify all required parameters for the command you are using. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values
* Refer to the following links for guidance on specific features:

    | Operation/feature | Single server | Flexible server |
    |--|--|--|
    |Create server|[Quickstart](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)|[Quickstart](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-server-cli)|
    |Public access & firewall rules|[Manage firewall](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli)|[Manage Public access](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-cli)|
    |Private access & VNet|[VNet service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli)<br>[Manage Private Link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-cli)|[Manage Private access](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-cli)|
    |Restore|[Perform restore](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)|[Perform restore](https://docs.microsoft.com/azure/mysql/flexible-server)|
    |Replication|[Manage replicas](https://docs.microsoft.com/azure/mysql/howto-read-replicas-cli)|[Manage replicas](https://docs.microsoft.com/azure/mysql/flexible-server)|
    |Server parameters|[Configure parameters](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli)|[Configure parameters](https://docs.microsoft.com/azure/mysql/flexible-server)|
    |Move server across resource groups or subscriptions|[Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)|

## **Recommended Documents**

* [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [Azure Database for MySQL CLI sample script collection](https://docs.microsoft.com/azure/mysql/sample-scripts-azure-cli)