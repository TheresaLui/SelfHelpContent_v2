<properties
    pageTitle="Commons Issues with using Azure Database Migration Services"
    description="Commons Issues with using Azure Database Migration Services"
    service="microsoft.dbformysql"
    resource="servers"
    authors="mksuni"
    ms.author="bahusse,jtoland"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32747556"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f4dcad6d-caa7-462c-b670-c4c51ac2adf2"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Common issues with using Azure Database Migration Services

You can do online and offline migrations using Azure database migration services (DMSs). Most users can resolve common issues by using the following steps.

## **Recommended Steps**

* **Error 1227 "Access denied; you need (at least one of) the SUPER privilege(s) for this operation"**<br>
  This error occurs after importing a dump file that contains definers. Although Azure Database for MySQL is a managed PaaS solution and SUPER privileges are restricted, you can enable [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) so that you can create definers without issue.

  For more information, see [ERROR 1227 (42000) at line 101: Access denied; you need (at least one of) the SUPER privilege(s) for this operation. Operation failed with exitcode 1](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1227-42000-at-line-101-access-denied-you-need-at-least-one-of-the-super-privileges-for-this-operation-operation-failed-with-exitcode-1).

* **Got error 1 from storage engine?**<br>
  See [Can't restore database with error "Got error 1 from storage engine"](https://techcommunity.microsoft.com/t5/azure-database-support-blog/azure-database-for-mysql-8211-can-t-restore-database-with-error/ba-p/368896)

* **Upgrade MySQL 5.6 to MySQL 5.7?**<br>
  See [Major version upgrade FAQs](https://docs.microsoft.com/azure/mysql/how-to-major-version-upgrade#frequently-asked-questions) and this [tutorial about how to upgrade using Azure portal](https://docs.microsoft.com/azure/mysql/how-to-major-version-upgrade#perform-major-version-upgrade-from-mysql-56-to-mysql-57-using-azure-portal) or [CLI](https://docs.microsoft.com/azure/mysql/how-to-major-version-upgrade#perform-major-version-upgrade-from-mysql-56-to-mysql-57-using-azure-cli).

* **Migrate Azure Database for MySQL server to another region?**<br>
  See [Move an Azure Database for MySQL server to another region by using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-move-regions-portal) or you may consider [Migrate your MySQL database to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore) and read [Move Azure Database for MySQL server into a different Azure subscription](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/restore-your-azure-database-for-mysql-server-into-a-different/ba-p/1043570).

* **Migrate Azure Database for MySQL server to another subscription or resource group?**<br>
  See [Move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription#use-the-portal)

* **Azure portal says MySQL version 5.7 or 8.0, but the application is showing 5.6.47.0**<br>
  Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To connect to gateway that is version MySQL 5.7 using port number 3308 instead of 3306 and to connect through gateway that is running MySQL version 8.0 connect via port 3309.

  **Connection string examples:**
  * Gateway 5.7: mysql -h servername.mysql.database.azure.com -u username@servername -P 3308 -p
  * Gateway 8.0: mysql -h servername.mysql.database.azure.com -u username@servername -P 3309 -p

* Verify the steps for migrating databases from **RDS MySQL** instance to **Azure Database for MySQL** using [this example of how to migrate from RDS to Single server](https://docs.microsoft.com/azure/dms/tutorial-rds-mysql-server-azure-db-for-mysql-online).

* Verify steps for migrating from **on-premises MySQL** instance to **Azure Database for MySQL** Single server using [this example for online migration with MySQL](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online).

* See [known issues with DMS](https://docs.microsoft.com/azure/dms/known-issues-azure-mysql-online)

## **Recommended Documents**

* [Troubleshoot errors when connecting to source database](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms-source-connectivity)
* [Common issues with DMS](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)
