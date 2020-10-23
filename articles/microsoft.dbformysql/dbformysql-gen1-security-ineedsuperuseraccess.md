<properties
    pageTitle="Managing permissions in Azure Database for MySQL Single Server"
    description="Managing permissions in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="420"
    selfHelpType="generic"
    supportTopicIds="32747566"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7f400acd-6be4-42c2-a5d8-e39b5c729af8"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Managing permissions in Azure Database for MySQL Single Server

User permissions for database user are managed through the MySQL built-in user management capabilities. Users can be created through SQL statements or tools like MySQL Workbench. Please note that super user access cannot be granted in the managed service.

## **Recommended Steps**

* DBA and super user privileges are not supported. The administrator user (created during new server creation), allows you to perform most of DDL and DML statements.
* Review the current [service limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
* If you lose your admin account password or you need to change the password, follow the [reset password article](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal#update-admin-password) to update the password
* For more information on how to manage users and roles in MySQL, please refer to the [MySQL community edition documentation](https://dev.mysql.com/doc/refman/5.7/en/access-control.html)

## **Recommended Documents**

* [Create users in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-users)<br>
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)<br>
* [Azure Database for MySQL Single Server - Limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
