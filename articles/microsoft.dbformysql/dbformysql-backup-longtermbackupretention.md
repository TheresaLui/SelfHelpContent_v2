<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="120"
    selfHelpType="generic"
    supportTopicIds="32640067"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="be30fc87-a22e-47e3-b1b5-7a80dc1b3a12"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL

Long term retention backups are currently not natively supported by the service. You have the option to use **mysqldump** to take backups and store them for long term retention. Third party solutions like [Commvault](https://documentation.commvault.com/commvault/v11/article?p=111861.htm) are available.

Native support for long term retention backups is currently being worked on by the Azure engineering team. However, you can use alternative solution to back your data for long term retention capabilities. 

## **Recommended Steps**

For long term backup retention of backups, you have following options:

*   You can write a script to use mysqldump to backup your databases, and copy the dumpfile to Azure blob storage and automate to run it weekly, monthly or yearly based on your archival strategy. Our team has blogged a [step by step article](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/automate-backups-of-your-azure-database-for-mysql-server-to/ba-p/1791157) to achieve it.
*   We have partnered with CommVault to provide [long term retention for Azure DB for MySQL](https://www.commvault.com/collaborating-to-enhance-azure-paas-database-long-term-retention)
*   For Logs retention, you can archive logs to storage account. Refer to link [here](https://docs.microsoft.com/bs-latn-ba/azure/mysql/howto-configure-audit-logs-portal#set-up-diagnostic-logs)

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity)<br>
* [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/concepts-backup)
