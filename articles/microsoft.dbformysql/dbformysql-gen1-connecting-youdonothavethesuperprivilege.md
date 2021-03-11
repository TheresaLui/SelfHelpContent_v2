<properties
  pagetitle="ERROR 1419: You do not have the SUPER privilege and binary logging is enabled "
  description="ERROR 1419: You do not have the SUPER privilege and binary logging is enabled "
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="bahusse, jtoland"
  selfhelptype="Generic"
  supporttopicids="32788631"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="cd112372-00e8-49a4-91bc-218b84ff271f"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# ERROR 1419: You do not have the SUPER privilege and binary logging is enabled

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

* **ERROR 1419 (HY000) at line 101: You do not have the SUPER privilege and binary logging is enabled**

  To mitigate the issue, you need to enable [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) from the **Parameters** blade in the Azure portal.

* **ERROR 1045 (28000): Access denied for user 'username'@'IP address' (using password: YES)”?**

  Ensure that the "username" exists as a valid user on the server, as it may have been inadvertently deleted.

  Use MySQL Workbench to check **Users and Privileges**, or run the following query:

  `select user from mysql.user;`

  This provides a list of all users that can connect to help you determine if the host IP is allowed to connect for the user in question. You may be able to connect with another user from the list.

* **Error 1227 “Access denied; you need (at least one of) the SUPER privilege(s) for this operation”**

  This error occurs after importing a dump file that contains definers. While Azure Database for MySQL is a managed PaaS solution and SUPER privileges are restricted, you can enable [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) so that you can create definers without issue.

## **Recommended documents**

* Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
* Azure Database for MySQL backup and restore concepts for [Single Server](https://docs.microsoft.com/azure/mysql/concepts-backup) and [Flexible Servers](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore)
* How-to restore a MySQL server using the Azure portal [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)
* How-to restore a MySQL server using the Azure CLI [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
* [How to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
