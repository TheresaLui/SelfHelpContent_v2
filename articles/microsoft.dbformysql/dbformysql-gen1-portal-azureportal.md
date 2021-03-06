<properties
    pageTitle="Using Azure Portal for Azure Database for MySQL Single Server"
    description="Using Azure Portal for Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela,ltoland"
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

Azure Database for MySQL Single Server provides easy management of servers through the Azure portal. You can resolve common issues by using the following guidance.

## **Recommended Steps**

* **Azure portal says MySQL version 5.7 or 8.0, but the application is showing 5.6.47.0**<br>
Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To connect to the gateway that is version MySQL 5.7,  use port number 3308 instead of 3306. To connect through a gateway that is running MySQL version 8.0, use port 3309.

  **Connection string examples:**<br>
  * Gateway 5.7: mysql -h servername.mysql.database.azure.com -u username@servername -P 3308 -p
  * Gateway 8.0: mysql -h servername.mysql.database.azure.com -u username@servername -P 3309 -p

* **Export Database Backup?**<br>
Azure Database for MySQL takes backups of the data files and the transaction log. These backup files are not user-exposed and cannot be exported. You can [Back up Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/backup-azure-database-for-mysql-to-a-blob-storage/ba-p/803830)

* **Performance Recommendation timeout?**<br>
   [Auto Stop and Start your Azure Database for MySQL Single Server](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/auto-stop-and-start-your-azure-database-for-mysql-single-server/ba-p/1955740)

### Quick Tips
Check that the issue is not caused by browser cache. Use a different browser or a different client machine. If you don't have other browsers, try an InPrivate session in Edge or an incognito session in Chrome.

## **Recommended Documents**

* [Create server - Quickstart](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-portal)
* [Firewall rules - Manage rules](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal/)
* [Manage VNet service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)
* [Manage Private Link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* [Perform restore](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal/)
* [Manage replicas](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal/)
* [Configure parameters](https://docs.microsoft.com/azure/mysql/howto-server-parameters/)
* [Monitor Server - Configure alerts](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric/)|howto-database-threat-protection-portal/)
* [Move server across resource groups or subscriptions - Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
* [Azure Database for MySQL Single Server documentation](https://docs.microsoft.com/azure/mysql/single-server)
