<properties
	pageTitle="Connection issues to MySQL"
	description="Connection issues to MySQL"
	service="microsoft.dbformysql"
	resource="servers"
	authors="ankam"
    ms.author="ankam,janeng"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds="32640053,32640055,32640058,32640090"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="3415dc33-5b6f-46ff-a1e8-6b33624af192"
/>

# Connection issues to Azure Databases for MySQL

Persistent connection issues to Azure Databases for MySQL can occur due to incorrect firewall configuration, incorrect connection string, and other causes. Work through the recommended steps to ensure you are not hitting a misconfiguration problem.

## **Recommended Steps**

* [Set up firewall rules](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) to allow the client IP address
* Follow [connection recommendations](https://docs.microsoft.com/azure/mysql/concepts-connection-libraries) on computers that host your client program
* Fix [incorrect connection strings](https://docs.microsoft.com/azure/mysql/howto-connection-string) in your application

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
