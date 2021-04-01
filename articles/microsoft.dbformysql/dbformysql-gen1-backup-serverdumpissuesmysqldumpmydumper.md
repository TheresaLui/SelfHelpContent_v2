<properties
  pagetitle="Issues with backup using mysqldump and myDumper"
  description="Issues with backup using mysqldump and mydumper"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="sumuth,pariks,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747585"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a8300a93-870a-4396-a250-5eae34feacf3"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Issues with backup using mysqldump and myDumper

You can back up your databases by using `mysqldump` and `myDumper` and then restore the databases to Azure Database for [MySQL - Single Server](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) or [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal#create-a-firewall-rule-after-server-is-created).

You can resolve common error messages by using the following steps.

## **Recommended Steps**

* Error message like **"MySQL has gone away"** or **"Lost connection to MySQL server during query"** during backup.<br>

  To resolve the error, increase the `max_allowed_packet`, `net_write_timeout`, and `net_read_timeout` values to appropriate levels.

* Error message like **access denied** when trying to run the command.<br>

  Review the firewall configuration of your MySQL - Single Server or Flexible Server.

* Error message like **"SSL connection is required. Please specify SSL options and retry."**<br>

  Check if you have the parameter `–SSL=1` in your `mysqldump` command, as shown below:

  ```
  mysqldump -h servername -u username -p –ssl=1 dbname > filename
  ```

* **Backing up (Exporting) Azure Database for MySQL to Blog Storage**<br>
For step-by-step instructions, see [Back up Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830).

* **Error 1227 "Access denied; you need (at least one of) the SUPER privilege(s) for this operation"**<br>
This error occurs after importing a dump file that contains definers. Although Azure Database for MySQL is a managed PaaS solution and SUPER privileges are restricted, you can enable [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) so that you can create definers without issue.

For more information, see [ERROR 1227 (42000) at line 101: Access denied; you need (at least one of) the SUPER privilege(s) for this operation. Operation failed with exitcode 1](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1227-42000-at-line-101-access-denied-you-need-at-least-one-of-the-super-privileges-for-this-operation-operation-failed-with-exitcode-1).

### Quick Tips

* Check the version of **`mysqldump`** or **`mysqldumper`** to make sure it's the same version as that of MySQL - Single Server or Flexible Server.
* See [all known issues](https://github.com/maxbube/myDumper/issues) for `myDumper` to determine if your issue is related to a known issue.

## **Recommended Documents**

* [`myDumper` documentation](https://github.com/maxbube/myDumper)
* [`mysqldump` documentation](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)
