<properties
    pageTitle="Managing permissions in Azure Database for MySQL"
    description="Managing permissions in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="Bashar-MSFT"
    ms.author="bahusse"
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

## **Fix it yourself**

* **Reset server admin privileges?**
Resetting server admin password will automatically reset the server admin privileges to default. [How to reset password](https://docs.microsoft.com/en-us/azure/mysql/howto-create-manage-server-portal#update-admin-password)

* **Using Triggers or Definers?** Consider using [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) and [Tips and Tricks for Azure Database for MySQL Super user errors](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/tips-and-tricks-in-using-mysqldump-and-mysql-restore-to-azure/ba-p/916912)

* **Enabling or Disabling global server parameter** Azure Database for MySQL exposes the ability to change the value of various MySQL server parameters using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters), [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli), and [PowerShell](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-powershell) to match your workload's needs.

* **DBA and super user privileges** are not supported. The administrator user (created during new server creation), allows you to perform most of DDL and DML statements. Review the current [service limitations](https://docs.microsoft.com/azure/mysql/concepts-limits) and [flexible server limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)

* **Manage users and roles in MySQL?** please refer to the [MySQL community edition documentation](https://dev.mysql.com/doc/refman/5.7/en/access-control.html)

## **Recommended Documents**

* [Create users in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-users)
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal)
* [Azure Database for MySQL Single Server - Limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
* [Azure Database for MySQL Flexible Server - Limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)