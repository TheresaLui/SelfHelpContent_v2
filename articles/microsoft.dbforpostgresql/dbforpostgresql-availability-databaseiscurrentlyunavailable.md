<properties
    pageTitle="Error: Server not available or SSL SYSCALL error: EOF detected"
    description="Error: Server not available or SSL SYSCALL error: EOF detected"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="20"
    selfHelpType="generic"
    supportTopicIds="32639974"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="6428cfa2-9135-430c-8f96-96c8768e01d1"
/>

# Error: Server not available or SSL SYSCALL error: EOF detected

The "SSL SYSCALL error: EOF detected" message, dropped connections, and other transient connection errors can occur when your PostgreSQL server is restarting. A restart happens when a service update is rolled out to your server, a technical issue with the underlying infrastructure was encountered, you triggered a restart of the server, you changed the compute resources, or you change between service tiers. The error you are seeing is transient and generally goes away in less than 60 seconds.

## **Recommended Steps**

* Try to reconnect to your server. If you can reconnect, consider [implementing retry logic](https://docs.microsoft.com/azure/postgresql/concepts-connectivity) to handle such transient errors and avoid application downtime.
* Check **Resource health** for your server to see if there were any reported events on the service side that could have caused the connection disruption.

## **Recommended Documents**

* [Troubleshoot connection issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
