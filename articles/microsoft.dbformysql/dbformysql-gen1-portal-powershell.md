<properties
    pageTitle="Using PowerShell for Azure Database for MySQL Single Server"
    description="Using PowerShell for Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="310"
    selfHelpType="generic"
    supportTopicIds="32747576"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="174d98eb-72a9-4d18-a2cd-3500fdbf22c3"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Using PowerShell for Azure Database for MySQL Single Server

Managing your Azure Database for MySQL Single Server using PowerShell. The module is is available in **preview**.

## Recommended Steps

* While the Az.MySql PowerShell module is in *preview for Azure Database for MySQL Single Server*, you must install it separately from the Az PowerShell module using the following command: `Install-Module -Name Az.MySql -AllowPrerelease`.
* If this is your first time using the Azure Database for MySQL service, you must register the Microsoft.DBforMySQL resource provider using `Register-AzResourceProvider -ProviderNamespace Microsoft.DBforMySQL`
* Refer to the following:
  * Creating a server, review [Create an Azure Database for MySQL Single Server using PowerShell](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-powershell)
  * Restoring a server, review [Restore Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-restore-server-powershell)
  * Creating replicas, review [Create read replica in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-read-replicas-powershell)
  * Configuring server parameters, review [Configure server parameters in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-powershell)
  * Enabling storage auto-grow, review [Enable auto grow in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-auto-grow-storage-powershell)
* Once the Az.MySql PowerShell module for single server is generally available, it becomes part of future Az PowerShell module releases and available natively from within Azure Cloud Shell.

## **Recommended Documents**

* [Create an Azure Database for MySQL Single Server using PowerShell](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-powershell)