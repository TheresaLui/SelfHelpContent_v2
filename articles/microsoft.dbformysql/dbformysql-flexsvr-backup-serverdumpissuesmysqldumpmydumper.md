<properties
  pagetitle="Issues with backup using mysqldump and myDumper&#xD;"
  description="Issues with backup using mysqldump and mydumper"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="sumuth,pariks"
  selfhelptype="Generic"
  supporttopicids="32747637"
  resourcetags="servers,databases"
  productpesids="17344"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="9f6ab11f-d9a6-426d-8854-51849d8016f1"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Issues with backup using mysqldump and myDumper

You can back up your databases using `mysqldump` and `myDumper` and then restore the databases to Azure Database for [My SQL - Single Server](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) or [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal#create-a-firewall-rule-after-server-is-created).

* I see an error like "**MySQL has gone away**" or "**Lost connection to MySQL server during query**" during the backup.
Increase the `max_allowed_packet`, `net_write_timeout`, and `net_read_timeout` values to appropriate levels.

* I see an error like "**access denied**" when trying to run the command.
Review the firewall configuration of your My SQL - Single Server or Flexible Server.

* I see an error like **"SSL connection is required. Please specify SSL options and retry."** 
Check to see if you have the parameter `–ssl=1` in your `mysqldump` command, as shown below:

```
mysqldump -h servername -u username -p –ssl=1 dbname > filename
```

## **Recommended Steps**

* Check if the version of **`mysqldump`** or **`mysqldumper`** is the same version as that of MySQL - Single Server or Flexible Server
* Check [all known issues](https://github.com/maxbube/myDumper/issues) for `myDumper` to see if your issue is related to any known issues

## **Recommended Documents**

* [`myDumper` documentation](https://github.com/maxbube/myDumper)
* [`mysqldump` documentation](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)
