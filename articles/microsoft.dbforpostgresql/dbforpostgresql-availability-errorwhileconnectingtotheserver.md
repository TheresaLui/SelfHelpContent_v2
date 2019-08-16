<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="30"
    selfHelpType="resource"
    supportTopicIds="32639977"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="14dc0ce8-a36f-4736-bd56-48f33e04eddd"
/>

# Persistent connection errors

Persistent connection issues when connecting to Azure Databases for PostgreSQL can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect virtual network (VNet) configuration, missing permissions for the user that is trying to connect, and other reasons. Work through the recommended steps to ensure you are not hitting a misconfiguration issue.

## **Recommended Steps**

* [Set up firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules) to allow your client's IP address
* If you are using VNets, ensure that the [service endpoints](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal) are correctly configured. Note that the Basic tier does not support VNet service endpoints.
* Follow [connection recommendations](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries) on computers hosting your client programs
* Make sure you are using the correct [SSL configuration](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security)
* Make sure the user you are connecting with has the appropriate permissions

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
* [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
