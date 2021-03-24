<properties
    pageTitle="Commons Issues with using Azure Database Migration Services"
    description="Troubleshoot commons issues with using Azure Database Migration Services"
    service="microsoft.dbformysql"
    resource="servers"
    authors="mksuni"
    ms.author="bahusse"
    displayOrder="550"
    selfHelpType="generic"
    supportTopicIds="32747994"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="22c6c8d5-ae3d-4f83-baad-172099086db9"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Commons issues with using Azure Database Migration Services

You can do online and offline migrations using Azure database migration services (DMS). Most users can resolve common issues by using the following information.

## **Recommended Steps**

* **"Got error 1 from storage engine"**? See [Can't restore database with error "Got error 1 from storage engine"](https://techcommunity.microsoft.com/t5/azure-database-support-blog/azure-database-for-mysql-8211-can-t-restore-database-with-error/ba-p/368896)

* **Upgrade MySQL 5.6 to MySQL 5.7?** Review [Major version upgrade FAQs](https://docs.microsoft.com/azure/mysql/how-to-major-version-upgrade#frequently-asked-questions) and this [tutorial about how to upgrade using Azure portal](https://docs.microsoft.com/azure/mysql/how-to-major-version-upgrade#perform-major-version-upgrade-from-mysql-56-to-mysql-57-using-azure-portal) or [CLI](https://docs.microsoft.com/azure/mysql/how-to-major-version-upgrade#perform-major-version-upgrade-from-mysql-56-to-mysql-57-using-azure-cli)
* Verify steps for migrating databases from **RDS MySQL** instance to **Azure Database for MySQL** using this [example for how to migrate from RDS to Single server](https://docs.microsoft.com/azure/dms/tutorial-rds-mysql-server-azure-db-for-mysql-online)
* Verify steps for migrating from **on-premises MySQL** instance to **Azure Database for MySQL** Single Server using this [example for online migration with MySQL](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online)
* View [known issues with DMS](https://docs.microsoft.com/azure/dms/known-issues-azure-mysql-online)

## **Recommended Documents**

* [Troubleshoot errors when connecting to source database](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms-source-connectivity)
* [Common issues with DMS](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)
