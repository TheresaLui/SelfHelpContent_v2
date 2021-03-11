<properties
  pagetitle="ERROR 9002 (28000): FATAL: Invalid Username specified"
  description="ERROR 9002 (28000): FATAL: Invalid Username specified"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788516"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="8c956f14-305c-4856-95d3-f3f57469cd9c"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# ERROR 9002 (28000): FATAL: Invalid Username specified

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

* **ERROR 9002 (28000): FATAL: Invalid Username specified**

  Confirm that the username you are passing ends with the correct server name/hostname field. The username needs to be passed in the format username@servername.

* **Applications that don't accept the username@servername format**

  To make a connection for applications that don't accept the username@servername format, use ProxySQL connection pooler. For more information, see [Connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842).

## **Recommended documents**

* [Why is username@servername required to connect to Azure Database for MySQL?](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/why-is-username-servername-required-to-connect-to-azure-database/ba-p/1204525)
* [Investigating connection issues with Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/investigating-connection-issues-with-azure-database-for-mysql/ba-p/2121204)
* [Deploy ProxySQL as a service on Kubernetes using Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/deploy-proxysql-as-a-service-on-kubernetes-using-azure-database/ba-p/1105959)
* [Connect to Azure Database for MySQL using ProxySQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Load-balance-read-replicas-using-ProxySQL-in-Azure-Database-for/ba-p/880042)
* [Connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842)
