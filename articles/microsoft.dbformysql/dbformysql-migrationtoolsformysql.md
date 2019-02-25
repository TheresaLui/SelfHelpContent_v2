<properties
    pageTitle="Migration Tools for MySQL"
    description="Outlines details about Database Migration Service"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jtoland"
    ms.author="jtoland,ankam"
    displayOrder="200"
    selfHelpType="resource"
    supportTopicIds=" 32628392, 32628396"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="3d124d20-7bab-43ac-83ff-4766fe107900"
/>

# Migration tools for Azure Database for MySQL

You can use the Azure Database Migration Service to perform an online migration of MySQL databases running on-premises, in a virtual machine, or on Amazon RDS or EC2 to [Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/). Online migrations provide for minimal downtime to the application.

## **Recommended Steps**

* Address migration [prerequisites](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#prerequisites)
* [Migrate the schema](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#migrate-the-sample-schema) using the mysqldump utility
* [Register the Microsoft.DataMigration resource provider](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#register-the-microsoftdatamigration-resource-provider)
* [Create an instance](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#create-a-dms-instance) of the Azure Database Migration Service
* [Create a migration project](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#create-a-migration-project)
* [Specify source details](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#specify-source-details)
* [Specify target details](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#specify-source-details)
* [Run the migration](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#run-the-migration)
* [Monitor the migration](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#monitor-the-migration)
* [Perform migration cutover](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#perform-migration-cutover)

## **Recommended Documents**

* [Migrate MySQL to Azure Database for MySQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online)
* Database Migration Guide: [Migrate MySQL to Azure Database for MySQL](https://datamigration.microsoft.com/scenario/mysql-to-azuremysql)
