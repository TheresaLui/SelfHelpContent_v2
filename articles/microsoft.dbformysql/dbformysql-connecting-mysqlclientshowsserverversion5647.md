<properties
  pagetitle="MySQL Client shows server version 5.6.47"
  description="MySQL Client shows server version 5.6.47"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788518"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="211a75bc-4a64-4ffb-ba84-6f9265ec9b2a"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# MySQL Client shows server version 5.6.47

## Quick tips

* **Azure Portal shows version 8 or 5.7 but the terminal application shows version: 5.6.47.0**

  Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To determine the version of your MySQL server instance, at the MySQL prompt, use the following command:

  `SELECT VERSION();`

## **Recommended documents**

* [Supported Azure Database for MySQL server versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions)
