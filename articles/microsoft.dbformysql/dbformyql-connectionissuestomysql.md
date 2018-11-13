<properties
	pageTitle="Connection issues to MySQL"
	description="Connection issues to MySQL"
	service="microsoft.dbformysql"
	resource="servers"
	authors="ankam"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32628383,32628386,32628388,32628391,32628408,32628393"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
/>

# Connection issues to Azure Databases for MySQL

## **Recommended steps**

Persistent connection issues to Azure Databases for MySQL can occur due to incorrect firewall configuration, incorrect connection string and other causes. Work through the following checklist to assure you are not hitting a misconfiguration problem:

* [Set up firewall rules](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) to allow the client IP address
* Follow [connection recommendations](https://docs.microsoft.com/azure/mysql/concepts-connection-libraries) on computers that host your client program
* Fix [incorrect connection strings](https://docs.microsoft.com/azure/mysql/howto-connection-string) in your application

## **Recommended documents**

[Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>

[Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
