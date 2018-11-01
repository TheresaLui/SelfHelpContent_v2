<properties
	pageTitle="Connection issues to MySQL"
	description="Connection issues to MySQL"
	service="microsoft.dbformysql"
	resource="servers"
	authors="ankam"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32568715,32568711"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
/>

# Connection issues to Azure Databases for MySQL

## **Recommended steps**
Persistent connection issues to Azure Databases for MySQL can occur due to incorrect firewall configuration, incorrect connection string and other causes.

* Set up firewall rules to allow the client IP address.<br>
[Configure MySQL Azure firewall rules](https://docs.microsoft.com/en-us/azure/mysql/concepts-firewall-rules)
* Follow connection recommendations on computers that host your client program<br>
[Connection recommendations](https://docs.microsoft.com/en-us/azure/mysql/concepts-connection-libraries)
* Fix incorrect connection strings in your application.<br>
[Connection strings to Azure Databases for MySQL](https://docs.microsoft.com/en-us/azure/mysql/concepts-high-availability)

## **Recommended documents**
[Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/en-us/azure/mysql/concepts-high-availability/)<br>
[Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/en-us/azure/mysql/tutorial-design-database-using-portal/)
