<properties
  pagetitle="Error 1227, 1045 Access Denied Errors"
  description="Error 1227, 1045 Access Denied Errors"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788513"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="cc93f316-82be-4307-ae3d-e717c28970ea"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Access Denied Errors 1045, 1227 while connecting to Azure Database for MySQL server

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

* **ERROR 1045 (28000) "Access denied for user 'username'@'IP address' (using password: YES)"**

  - Ensure that the "username" exists as a valid user on the server, as it may have been inadvertently deleted.

  - Use MySQL Workbench to check **Users and Privileges**, or run the following query:

   `select user from mysql.user;`

    This provides a list of all users that can connect to help you determine if the host IP is allowed to connect for the user in question. You may be able to connect with another user from the list.  

  For more information, see [ERROR 1045 (28000): Access denied for user 'username'@'IP address' (using password: YES)](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1045-28000-access-denied-for-user-usernameip-address-using-password-yes).

* **Error 1227 "Access denied; you need (at least one of) the SUPER privilege(s) for this operation"**

  This error occurs after importing a dump file that contains definers. While Azure Database for MySQL is a managed PaaS solution and SUPER privileges are restricted, you can enable [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) so that you can create definers without issue.

  For more information, see [ERROR 1227 (42000) at line 101: Access denied; you need (at least one of) the SUPER privilege(s) for this operation. Operation failed with exitcode 1](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1227-42000-at-line-101-access-denied-you-need-at-least-one-of-the-super-privileges-for-this-operation-operation-failed-with-exitcode-1).

* **ERROR 1419 (HY000) at line 101: "You do not have the SUPER privilege and binary logging is enabled"**

  To mitigate the issue, enable [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) from Azure portal parameters blade.

  For more information, see [ERROR 1419: You do not have the SUPER privilege and binary logging is enabled (you might want to use the less safe log_bin_trust_function_creators variable)](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1419-you-do-not-have-the-super-privilege-and-binary-logging-is-enabled-you-might-want-to-use-the-less-safe-log_bin_trust_function_creators-variable).

## **Recommended documents**

* Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
* Azure Database for MySQL backup and restore concepts for [Single Server](https://docs.microsoft.com/azure/mysql/concepts-backup) and [Flexible Servers](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore)
* How-to restore a MySQL server using the Azure portal [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)
* How-to restore a MySQL server using the Azure CLI [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
* [How to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
