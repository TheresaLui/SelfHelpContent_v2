<properties
    pageTitle="Managing permissions in Azure Database for MySQL Single Server"
    description="Managing permissions in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="Bashar-MSFT"
    ms.author="bahusse"
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

Permissions for database users are managed through the MySQL built-in user management capabilities. Users can be created through SQL statements or tools like MySQL Workbench. Super user access cannot be granted in the managed service.

### **Fix it yourself**

* **Reset server admin privileges?**

   Resetting the server admin password automatically resets the server admin privileges to the default. [How to reset password](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal#update-admin-password)

* **Using Triggers or Definers?** 

   Consider using [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) and [Tips and Tricks for Azure Database for MySQL Super user errors](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/tips-and-tricks-in-using-mysqldump-and-mysql-restore-to-azure/ba-p/916912)

* **Enabling or Disabling global server parameter** 

   Azure Database for MySQL exposes the ability to change the value of various MySQL server parameters using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters), [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli), and [PowerShell](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-powershell) to match your workload's needs.

* **DBA and super user privileges are not supported.** 

   The administrator user (created during new server creation), allows you to perform most of DDL and DML statements. Review the current [service limitations](https://docs.microsoft.com/azure/mysql/concepts-limits).

* **Manage users and roles in MySQL?** 

   Refer to the [MySQL community edition documentation](https://dev.mysql.com/doc/refman/5.7/en/access-control.html)

## **Recommended Documents**

* [Create users in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-users)
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)
* [Azure Database for MySQL Single Server - Limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
* [Tips and Tricks in using mysqldump and mysql restore to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/tips-and-tricks-in-using-mysqldump-and-mysql-restore-to-azure/ba-p/916912)
* [Export and import MySQL users and privileges to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/export-and-import-mysql-users-and-privileges-to-azure-database/ba-p/916995)
