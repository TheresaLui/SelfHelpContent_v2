<properties
	pageTitle="Connection issues to MariaDB"
	description="Connection issues to MariaDB"
	service="microsoft.dbformariadb"
	resource="servers"
	authors="ajlam"
    ms.author="andrela"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds="32640118,32640123,32640152"
	resourceTags="servers, databases"
	productPesIds="16617"
	cloudEnvironments="public"
	articleId="mariadbconnectionissues"
/>

# Connection issues to Azure Databases for MariaDB

Persistent connection issues to Azure Databases for MariaDB can occur due to incorrect firewall configuration, incorrect connection string, and other causes. Work through the recommended steps to assure you are not hitting a misconfiguration problem.

## **Recommended Steps**

* [Set up firewall rules](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules) to allow the client IP address
* Follow [connection recommendations](https://docs.microsoft.com/azure/mariadb/concepts-compatibility) on computers that host your client program
* Fix [incorrect connection strings](https://docs.microsoft.com/azure/mariadb/howto-connection-string) in your application

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)