<properties
    pageTitle="Using Azure CLI for Azure Database for MySQL Flexible Server"
    description="Using Azure CLI for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="280"
    selfHelpType="generic"
    supportTopicIds="32747602"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="441a9b4d-b1b1-4915-8151-f8cfd6ca374a"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Using Azure CLI for Azure Database for MySQL Flexible Server

Azure Database for MySQL Flexible Server can be managed through the Azure CLI. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you may have to poll the status of the operation when using Azure CLI.

## **Recommended Steps**

* Make sure you are signed-in to the correct using **`az login`**
* You are using the correct subscription in case you have more than one
* You specify all required parameters for the command you are using. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values
* Refer to the following links for guidance on specific features:

    | Operation/feature | Flexible server |
    |--|--|
    |Create server|[Quickstart](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-server-cli)|
    |Public access (allowed IP addresses)|[Manage Public access](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-cli)|
    |Private access (VNet Integration)|[Manage Private access](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-cli)|
    |Restore|[Perform restore](https://docs.microsoft.com/azure/mysql/flexible-server)|
    |Replication|[Manage replicas](https://docs.microsoft.com/azure/mysql/flexible-server)|
    |Server parameters|[Configure parameters](https://docs.microsoft.com/azure/mysql/flexible-server)|
    |Monitor server|[Configure alerts](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-alert-on-metric)|
    |Move server across resource groups or subscriptions|[Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)|

## **Recommended Documents**

* [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)