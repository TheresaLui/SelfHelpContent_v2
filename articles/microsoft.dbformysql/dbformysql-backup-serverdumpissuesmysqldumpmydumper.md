<properties
  pagetitle="Issues with backup using mysqldump and myDumper&#xD;"
  description="Issues with backup using mysqldump and myDumper"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="sumuth,pariks"
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

* I see an error like **MySQL has gone away** or **Lost connection to MySQL server during query** during the backup.

Increase the **max_allowed_packet**, **net_write_timeout**, and **net_read_timeout** values to appropriate levels.

* I see an error like **access denied** error when trying to run the command.

**Review the firewall configuration** of your [My SQL - Single Server](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) or [Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal#create-a-firewall-rule-after-server-is-created).

* I see an error like **"SSL connection is required. Please specify SSL options and retry."**

Check to see if you have parameter `–SSL=1` in your `mysqldump` command. if not, add this parameter and then rerun the command:

```
mysqldump -h servername -u username -p –ssl=1 dbname > filename
``` 

### **Best Practices** 

* Check the version of `mysqldump` or `mysqldumper` to make sure they are the same version as MySQL - Single Server or Flexible Server.
* Check all [known issues for `myDumper`](https://github.com/maxbube/myDumper/issues) and see if your issue is related to any of these issues.


## **Recommended Documents**

* [`myDumper` documentation](https://github.com/maxbube/myDumper)
* [`mysqldump` documentation](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)
