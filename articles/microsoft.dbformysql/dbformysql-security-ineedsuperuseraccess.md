<properties
    pageTitle="Managing permissions in Azure Database for MySQL"
    description="Managing permissions in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="430"
    selfHelpType="generic"
    supportTopicIds="32640062"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1914abe8-9057-40cd-a970-b67c9cf10fd2"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Managing permissions in Azure Database for MySQL

User permissions for database user are managed through the MySQL built-in user management capabilities. Users can be created through SQL statements or tools like MySQL Workbench. Please note that super user access cannot be granted in the managed service.

## **Recommended Steps**

* DBA and super user privileges are not supported. The administrator user (created during new server creation), allows you to perform most of DDL and DML statements.
* Review the current [single server limitations](https://docs.microsoft.com/azure/mysql/concepts-limits) and [flexible server limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)
* If you lose your admin account password or you need to change the password, follow the [reset password article](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal#update-admin-password) to update the password
* For more information on how to manage users and roles in MySQL, please refer to the [MySQL community edition documentation](https://dev.mysql.com/doc/refman/5.7/en/access-control.html)

## **Recommended Documents**

* [Create users in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-users)<br>
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)<br>
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal)<br>
* [Azure Database for MySQL Single Server - Limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)<br>
* [Azure Database for MySQL Flexible Server - Limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)