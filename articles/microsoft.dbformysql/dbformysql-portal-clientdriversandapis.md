<properties
    pageTitle="Connecting to Azure Database for MySQL"
    description="Connecting to Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela,jtoland"
    displayOrder="340"
    selfHelpType="generic"
    supportTopicIds="32640049"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="021fc8cf-efdf-4aa3-98bb-85da3612195c"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connecting to Azure Databases for MySQL

Azure Database for MySQL uses the community edition of MySQL. As such, most drivers and tools are able to connect to the service. There are some limitations in functionality because Azure Database for MySQL is a fully managed platform as a service.

## **Fix it yourself**

* **Azure Portal says MySQL version 5.7 or 8.0, but the application is showing 5.6.47.0**
Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To connect to gateway that is version MySQL 5.7 using port number 3308 instead of 3306 and to connect through gateway that is running MySQL version 8.0 connect via port 3309.

   **Connection string examples:**

  * Gateway 5.7: mysql -h servername.mysql.database.azure.com -u username@servername -P 3308 -p
  * Gateway 8.0: mysql -h servername.mysql.database.azure.com -u username@servername -P 3309 -p

* Check the current [supported versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions) for the service.
* **Are you seeing the wrong server version?**<br>
  In the service, a gateway is used to redirect the connections to server instances. After the connection is established, the MySQL client displays the version of MySQL set in the gateway, not the actual version running on your MySQL server instance. To determine the version of your MySQL server instance, use the SELECT VERSION(); command at the MySQL prompt.
* [TLS considerations?](https://docs.microsoft.com/azure/mysql/how-to-connect-overview-single-server#tls-considerations-for-database-connectivity)
* Check the current known [limitations of the service](https://docs.microsoft.com/azure/mysql/concepts-limits) to verify that your scenario is supported.
* Review the list of officially [supported drivers](https://docs.microsoft.com/azure/mysql/concepts-compatibility) to make sure you are using a supported driver version.

## **Recommended documents**

* [Connect with PHP](https://docs.microsoft.com/azure/mysql/connect-php)<br>
* [Connect with Java](https://docs.microsoft.com/azure/mysql/connect-java)<br>
* [Connect with .NET](https://docs.microsoft.com/azure/mysql/connect-csharp)<br>
* [Connect with Python](https://docs.microsoft.com/azure/mysql/connect-python)<br>
* [Connect with Node.js](https://docs.microsoft.com/azure/mysql/connect-nodejs)<br>
* [Connect with Ruby](https://docs.microsoft.com/azure/mysql/connect-ruby)<br>
* [Connect with C++](https://docs.microsoft.com/azure/mysql/connect-cpp)<br>
* [Connect with Go](https://docs.microsoft.com/azure/mysql/connect-go)<br>
* [Connect with Workbench](https://docs.microsoft.com/azure/mysql/connect-workbench)