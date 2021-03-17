<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32780962"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-availability-errorwhileconnectingtotheserver"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Error while connecting to server

## **Recommended Steps**

### **Intermittent connection errors**

Causes of intermittent connection issues include server restart, high resource usage on the server, and client timeouts. The following steps can help you resolve the issue:

* Retry the connection to see if the problem persists
* When you see `An existing connection was forcibly closed by the remote host`, this indicates that your client closed the connection to the Postgres server. Check your client timeout and idle connection settings. [Learn more about this error](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/troubleshoot-postgresql-an-existing-connection-was-forcibly/ba-p/925164)
* Check your server metrics to see if any resource is near 100% usage. High usage can lead to unavailable resources for a new connection.
* Check the connection limit of your compute tier


### **Persistent connection errors**

If connection issues last for more than a couple minutes, the root cause may be a persistent issue. Persistent connection issues when connecting to Azure Database for PostgreSQL can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect virtual network (VNet) configuration, missing permissions for the user who is trying to connect, and other reasons. Work through the recommended steps to ensure you're not encountering a misconfiguration issue.

* Make sure the user you're connecting with has the appropriate permissions
* Make sure you are using TLS version 1.2 or higher
* If your server is in a virtual network, confirm that you are connecting from resources that have access to that virtual network
* If your server uses public access, confirm that the firewall rules include the resource you are connecting from
