<properties
    pageTitle="Node unavailable on Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Node unavailable on Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource="serverGroups"
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-connectivity-nodeunavailable.md"
    selfHelpType="resource"
    supportTopicIds="32731218"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Coordinator or worker node unavailable

## **Recommended Steps**
* The error *could not connect to server: Connection timed out. Is the server running on host and accepting TCP/IP connections on port 5432* typically indicates a firewall rule is needed. [Set up a firewall rule](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-manage-firewall-using-portal) to allow your client's IP address.
* Check the [resource metrics](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-monitoring) for the node. If the node is at capacity for a resource like CPU, memory, IO, or storage, consider reducing activity on the cluster or [scaling up](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-scaling).
* [Troubleshoot connection issues](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-troubleshoot-common-connection-issues)

