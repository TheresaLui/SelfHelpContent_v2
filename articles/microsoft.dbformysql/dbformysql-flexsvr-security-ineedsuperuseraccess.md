<properties
    pageTitle="Managing permissions in Azure Database for MySQL Flexible Server"
    description="Managing permissions in Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="390"
    selfHelpType="generic"
    supportTopicIds="32747619"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ac904f12-3010-49c6-ac35-16c55a563619"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Managing permissions in Azure Database for MySQL Flexible Server

User permissions for database user are managed through the MySQL built-in user management capabilities. Users can be created through SQL statements or tools like MySQL Workbench. Please note that super user access cannot be granted in the managed service.

## **Recommended Steps**

* DBA and super user privileges are not supported. The administrator user (created during new server creation), allows you to perform most of DDL and DML statements.
* Review the current [service limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)
* If you lose your admin account password or you need to change the password, follow the [reset password article](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal#reset-admin-password) to update the password
* For more information on how to manage users and roles in MySQL, please refer to the [MySQL community edition documentation](https://dev.mysql.com/doc/refman/5.7/en/access-control.html)

## **Recommended Documents**

* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal)<br>
* [Azure Database for MySQL Flexible Server - Limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)
