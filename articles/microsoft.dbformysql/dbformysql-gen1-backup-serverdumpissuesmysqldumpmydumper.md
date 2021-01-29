<properties
  pagetitle="Issues with backup using mysqldump and myDumper"
  description="Issues with backup using mysqldump and mydumper"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="sumuth,pariks"
  selfhelptype="Generic"
  supporttopicids="32747585"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a8300a93-870a-4396-a250-5eae34feacf3"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Issues with backup using mysqldump and myDumper

You can back up your databases using `mysqldump` and `myDumper` and then restore the databases to Azure Database for [MySQL - Single Server](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) or [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal#create-a-firewall-rule-after-server-is-created).

* I see an error like **MySQL has gone away** or **Lost connection to MySQL server during query** during the backup.
To resolve the error, increase the `max_allowed_packet`, `net_write_timeout`, and `net_read_timeout` values to appropriate levels.

* I see an error like **access denied** error when trying to run the command.
Review the firewall configuration of your MySQL - Single Server or Flexible Server.

* I see an error like **"SSL connection is required. Please specify SSL options and retry."** 
Check if you have the parameter `–SSL=1` in your `mysqldump` command, as shown below:

```
mysqldump -h servername -u username -p –ssl=1 dbname > filename
```

## **Recommended Steps**

* Check the version of **`mysqldump`** or **`mysqldumper`** to make sure it's the same version as that of MySQL - Single Server or Flexible Server
* See [all known issues](https://github.com/maxbube/myDumper/issues) for `myDumper` to see if your issue is related to any of the known issues

## **Recommended Documents**

* [`myDumper` documentation](https://github.com/maxbube/myDumper)
* [`mysqldump` documentation](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)
