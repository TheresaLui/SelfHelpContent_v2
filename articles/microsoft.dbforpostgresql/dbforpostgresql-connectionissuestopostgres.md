<properties
	pageTitle="Connection issues to PostgreSQL"
	description="Connection issues to PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="ankam"
    ms.author="anakm, janeng"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32628432,32628438,32628441,32628458,32628443"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="48fb0d99-c2ee-4558-a91a-ef9940c31c5b"
/>

# Connection issues to Azure Databases for PostgreSQL

Persistent connection issues to Azure Databases for PostgreSQL can occur due to incorrect firewall configuration, incorrect connection string, and other causes. Work through the following recommended steps to assure you are not hitting a misconfiguration problem.

## **Recommended Steps**

* [Set up firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules/) to allow the client IP address
* Follow [connection recommendations](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries) on computers that host your client program
* Fix incorrect connection strings in your application. Go to the [Azure Portal](https://portal.azure.com) and click on the "**Connection Strings**" blade to see sample connection strings.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to PostgreSQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
