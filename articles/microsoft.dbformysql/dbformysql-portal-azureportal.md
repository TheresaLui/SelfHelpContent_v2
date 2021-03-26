<properties
    pageTitle="Using Azure Portal for Azure Database for MySQL"
    description="Using Azure Portal for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="andrela"
    ms.author="ajlam,jtoland"
    displayOrder="290"
    selfHelpType="generic"
    supportTopicIds="32640048"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dc501f13-9441-4f1b-936f-4f399e5eea5d"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Using Azure Portal for Azure Database for MySQL

Azure Database for MySQL offers two deployment types - single server and flexible server. Both types of servers can be managed through the Azure portal.

## Fix it yourself

* **Azure Portal says MySQL version 5.7 or 8.0, but the application is showing 5.6.47.0**<br>
Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To connect to gateway that is version MySQL 5.7 using port number 3308 instead of 3306 and to connect through gateway that is running MySQL version 8.0 connect via port 3309.

   **Connection string examples:**<br>
  * Gateway 5.7: mysql -h servername.mysql.database.azure.com -u username@servername -P 3308 -p<br>
  * Gateway 8.0: mysql -h servername.mysql.database.azure.com -u username@servername -P 3309 -p

* **Export database backup?**<br>
   Azure Database for MySQL takes backups of the data files and the transaction log. These backup files are not user-exposed and cannot be exported. You can [Back up Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/backup-azure-database-for-mysql-to-a-blob-storage/ba-p/803830).

* **Performance Recommendation timeout?**<br>
   [Auto Stop and Start your Azure Database for MySQL Single Server](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/auto-stop-and-start-your-azure-database-for-mysql-single-server/ba-p/1955740)

  Refer to the following links for guidance on specific features:

    | Operation/feature | Single server | Flexible server |
    |--|--|--|
    |Create server|[Quickstart](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-portal)|[Quickstart](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-server-portal)|
    |Public access & firewall rules|[Manage firewall](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal/)|[Manage Public access](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal)|
    |Private access & VNet|[Manage VNet service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)<br>[Manage Private Link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)|[Manage Private access](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-portal)|
    |Restore|[Perform restore](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal/)|[Perform restore](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)|
    |Replication|[Manage replicas](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal/)|[Manage replicas](https://docs.microsoft.com/azure/mysql/flexible-server)|
    |Server parameters|[Configure parameters](https://docs.microsoft.com/azure/mysql/howto-server-parameters/)|[Configure parameters](https://docs.microsoft.com/azure/mysql/flexible-server)|
    |Monitor server|[Configure alerts](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric/)|[Configure alerts](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-alert-on-metric)|
    |Move server across resource groups or subscriptions|[Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)|

## Quick tip

Use a different browser or client computer to verify that the issue is not caused by your browser cache. If you don't have other browsers, please try a private session in your internet browser.

## **Recommended documents**

* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)