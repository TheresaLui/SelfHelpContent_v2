<properties
    pageTitle="Issues with migrating to Azure Database for MySQL"
    description="Outlines issues that customers might encounter during migration"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jtoland"
    ms.author="jtoland,ankam"
    displayOrder="20"
    selfHelpType="resource"
    supportTopicIds=" 32640064"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="f08de132-b511-4a81-a2f1-ecf5358f8a7a"
/>

# Issues with migrating to Azure Database for MySQL

Migrating a database server can have many facets and the best method to use depends on many factors such as: How much data needs to be moved, can downtime be tolerated, does your application move as well, and so on.

Most migration problems can be solved by working through the recommended steps.

## **Recommended Steps**

* If you are evaluating different migration options, consult our [Azure Database Migration Guide](https://datamigration.microsoft.com/)
* If you are migrating yourself (e.g. using dump and restore, or data-in-replication) and encounter problems, consider using the [Data Migration Service](https://azure.microsoft.com/services/database-migration/)
* If you are using the Data Migration Service and experience problems, work thought the [step-by-step tutorials for Azure Database for MySQL](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online)
  * Address issues with [online migration configuration](https://docs.microsoft.com/azure/dms/known-issues-azure-mysql-online#online-migration-configuration)
  * Address [datatype limitations](https://docs.microsoft.com/azure/dms/known-issues-azure-mysql-online#datatype-limitations)
  * Address [LOB limitations](https://docs.microsoft.com/azure/dms/known-issues-azure-mysql-online#lob-limitations)
  * Address [other common issues](https://docs.microsoft.com/azure/dms/known-issues-azure-mysql-online#other-limitations)

## **Recommended Documents**

* [Azure Database for MySQL](https://docs.microsoft.com/azure/mysql)<br>
* [Azure Database Migration Guide](https://datamigration.microsoft.com/)<br>
* [Data Migration Service](https://azure.microsoft.com/services/database-migration/)

