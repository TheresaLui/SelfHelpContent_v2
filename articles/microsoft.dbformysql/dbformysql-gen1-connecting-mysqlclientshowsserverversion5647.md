<properties
  pagetitle="MySQL Client shows server version 5.6.47"
  description="MySQL Client shows server version 5.6.47"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="bahusse, jtoland"
  selfhelptype="Generic"
  supporttopicids="32788633"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="8f2ad8c1-ed34-4965-b8d8-4a4d01a525ca"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# MySQL Client shows server version 5.6.47

## **Recommended Steps**

* **Azure Portal shows version 8 or 5.7, but the terminal application shows version: 5.6.47.0**

Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To determine the version of your MySQL server instance, at the MySQL prompt, use the following command:

  `SELECT VERSION();`

You can connect to a gateway that is version MySQL 5.7 by using port number 3308 instead of 3306. In addition, you can connect through a gateway that is running MySQL version 8.0 by using port 3309.

  **Connection string examples:**<br>
  * Gateway 5.7: mysql -h servername.mysql.database.azure.com -u username@servername -P 3308 -p<br>
  * Gateway 8.0: mysql -h servername.mysql.database.azure.com -u username@servername -P 3309 -p

## **Recommended Documents**

* [Supported Azure Database for MySQL server versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions)
