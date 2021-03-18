<properties
    pageTitle="Using Azure Portal for Azure Database for MySQL Single Server"
    description="Using Azure Portal for Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="290"
    selfHelpType="generic"
    supportTopicIds="32747548"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5df358bd-ffdf-4b85-81ed-d3664fb38560"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Using Azure Portal for Azure Database for MySQL Single Server

Azure Database for MySQL Single Server provides easy management of servers through the Azure portal.

* **Are you seeing wrong server version?** 

   In the service, a gateway is used to redirect the connections to server instances. After the connection is established, the MySQL client displays the version of MySQL set in the gateway, not the actual version running on your MySQL server instance. To determine the version of your MySQL server instance, use the `SELECT VERSION();` command at the MySQL prompt.

* **Export Database Backup?** 

   Azure Database for MySQL takes backups of the data files and the transaction log. These backup files are not user-exposed and cannot be exported. You can [Back up Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/backup-azure-database-for-mysql-to-a-blob-storage/ba-p/803830)

* **Performance Recommendation timeout?**

   [**Auto Stop and Start your Azure Database for MySQL Single Server**](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/auto-stop-and-start-your-azure-database-for-mysql-single-server/ba-p/1955740)

## **Recommended Documents**

* If you are having problems, review the following docs:

    | Operation/feature | Single server |
    |--|--|
    |Create server|[Quickstart](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-portal)|
    |Firewall rules|[Manage rules](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal/)|
    |VNet service endpoints|[Manage VNet service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)|
    |Private Link|[Manage Private Link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)|
    |Restore|[Perform restore](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal/)|
    |Replication|[Manage replicas](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal/)|
    |Server parameters|[Configure parameters](https://docs.microsoft.com/azure/mysql/howto-server-parameters/)|
    |Monitor server|[Configure alerts](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric/)|howto-database-threat-protection-portal/)|
    |Move server across resource groups or subscriptions|[Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)|

* Check that the issue is not caused by browser cache. Use a different browser or a different client machine. If you don't have other browsers, try an InPrivate session in Edge or an incognito session in Chrome.
* [Azure Database for MySQL Single Server documentation](https://docs.microsoft.com/azure/mysql/single-server)
