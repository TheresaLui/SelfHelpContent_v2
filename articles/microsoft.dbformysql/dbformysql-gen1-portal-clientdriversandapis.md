<properties
    pageTitle="Connecting to Azure Databases for MySQL Single Server"
    description="Connecting to Azure Databases for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    ms.author="bahuss,jtoland"
    displayOrder="300"
    selfHelpType="generic"
    supportTopicIds="32747551"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f163c7a1-176a-4076-b027-d38ace1d4ce2"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connecting to Azure Databases for MySQL Single Server

Azure Database for MySQL Single Server uses the community edition of MySQL. As such, most drivers and tools are able to connect to the service. There are some limitations in functionality because Azure Database for MySQL is a fully managed platform as a service.

## Fix it yourself

* Check the current [supported versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions) for the service.
* **Are you seeing the wrong server version?**<br>
  In the service, a gateway is used to redirect the connections to server instances. After the connection is established, the MySQL client displays the version of MySQL set in the gateway, not the actual version running on your MySQL server instance. To determine the version of your MySQL server instance, use the SELECT VERSION(); command at the MySQL prompt.
* [TLS considerations?](https://docs.microsoft.com/azure/mysql/how-to-connect-overview-single-server#tls-considerations-for-database-connectivity)
* Check the current known [limitations of the service](https://docs.microsoft.com/azure/mysql/concepts-limits) to verify that your scenario is supported.
* Review the list of officially [supported drivers](https://docs.microsoft.com/azure/mysql/concepts-compatibility) to ensure that you're using a supported driver version.

## **Recommended documents**

* [Connect with PHP](https://docs.microsoft.com/azure/mysql/connect-php)
* [Connect with Java](https://docs.microsoft.com/azure/mysql/connect-java)
* [Connect with .NET](https://docs.microsoft.com/azure/mysql/connect-csharp)
* [Connect with Python](https://docs.microsoft.com/azure/mysql/connect-python)
* [Connect with Node.js](https://docs.microsoft.com/azure/mysql/connect-nodejs)
* [Connect with Ruby](https://docs.microsoft.com/azure/mysql/connect-ruby)
* [Connect with C++](https://docs.microsoft.com/azure/mysql/connect-cpp)
* [Connect with Go](https://docs.microsoft.com/azure/mysql/connect-go)
* [Connect with Workbench](https://docs.microsoft.com/azure/mysql/connect-workbench)
