<properties
	pageTitle="Connection issues to PostgreSQL"
	description="Connection issues to PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="ankam"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32569391,32569392"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
/>

# Connection issues to Azure Databases for PostgreSQL

## **Recommended steps**
Persistent connection issues to Azure Databases for PostgreSQL can occur due to incorrect firewall configuration, incorrect connection string and other causes.

* Set up firewall rules to allow the client IP address <br>
[Configure PostgreSQL Azure firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules/)
* Follow connection recommendations on computers that host your client program <br>
[Connection recommendations](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries)
* Fix incorrect connection strings in your application <br>
[Connection strings to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-high-availability)

## **Recommended documents**
[Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-high-availability/)<br>
[Connecting to PostgreSQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
