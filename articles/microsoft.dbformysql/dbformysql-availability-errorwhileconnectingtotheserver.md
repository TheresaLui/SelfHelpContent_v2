<properties
    pageTitle="Connection issues to Azure Databases for MySQL"
    description="Connection issues to Azure Databases for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32640053"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="996e511f-55ca-4660-80d4-15a2aa76953b"
/>

# Connection issues to Azure Databases for MySQL

Persistent connection issues when connecting to Azure Databases for MySQL can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect VNet configuration, missing permissions for the user that is trying to connect, and others. Work through the recommended steps to ensure you are not hitting a misconfiguration problem.

## **Recommended Steps**

* [Set up firewall rules](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) to allow your client's IP address.
* If you are using VNets, ensure the correct configuration of the [service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal). Note that the Basic tier does not support VNet service endpoints.
* Follow [connection recommendations](https://docs.microsoft.com/azure/mysql/concepts-connection-libraries) on computers hosting your client programs
* Fix [incorrect connection strings](https://docs.microsoft.com/azure/mysql/howto-connection-string) in your application
* Make sure you are using the correct [SSL configuration](https://docs.microsoft.com/azure/mysql/howto-configure-ssl)
* Review the [supported client driver list](https://docs.microsoft.com/azure/mysql/concepts-compatibility) and ensure you are using a driver that is supported
* Make sure the user you are using has the appropriate permissions

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
