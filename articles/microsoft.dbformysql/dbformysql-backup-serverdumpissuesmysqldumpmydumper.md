<properties
  pagetitle="Issues with backup using mysqldump and myDumper&#xD;"
  description="Issues with backup using mysqldump and myDumper"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="sumuth,pariks,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747992"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="88598dd7-c578-4b47-b8ea-6b9f7b61748e"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Issues with backup using mysqldump and myDumper

You can back up your databases using `mysqldump` and `myDumper` and then restore the databases to Azure Database for MySQL - Single Server or Flexible Server.

Following are solutions to some of the most common issues encountered in this process.

## Fix it yourself

* I see an error like **MySQL has gone away** or **Lost connection to MySQL server during query** during backup.

  Increase the **max_allowed_packet**, **net_write_timeout**, and **net_read_timeout** values to appropriate levels.

* I see an error like **access denied** when trying to run the command.

  **Review the firewall configuration** of your [My SQL - Single Server](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) or [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal#create-a-firewall-rule-after-server-is-created).

* I see an error like **"SSL connection is required. Please specify SSL options and retry."**

  Check to see if you have parameter `–SSL=1` in your `mysqldump` command. If not, add this parameter and then rerun the command:

  ```
  mysqldump -h servername -u username -p –ssl=1 dbname > filename
  ```

* **Backing up (Exporting) Azure Database for MySQL to Blog Storage?**

  To back up Azure Database for MySQL to a Blob storage, see [Backup Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830)

* **Error 1227 "Access denied; you need (at least one of) the SUPER privilege(s) for this operation"**

  This error occurs after importing a dump file that contains definers. While Azure Database for MySQL is a managed PaaS solution and SUPER privileges are restricted, you can enable [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) so that you can create definers without issue.

  For more information, see [ERROR 1227 (42000) at line 101: Access denied; you need (at least one of) the SUPER privilege(s) for this operation. Operation failed with exitcode 1](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1227-42000-at-line-101-access-denied-you-need-at-least-one-of-the-super-privileges-for-this-operation-operation-failed-with-exitcode-1).

## **Quick tips**

* Check the version of `mysqldump` or `mysqldumper` to make sure they are the same version as MySQL - Single Server or Flexible Server.
* Check all [known issues for `myDumper`](https://github.com/maxbube/myDumper/issues) and see if your issue is related to any of these issues.

## **Recommended documents**

* [`myDumper` documentation](https://github.com/maxbube/myDumper)
* [`mysqldump` documentation](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)
