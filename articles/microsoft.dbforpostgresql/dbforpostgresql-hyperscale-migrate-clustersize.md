<properties
    pageTitle="Help with cluster sizing for Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Help with cluster sizing for Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource=""
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-migrate-clustersize.md"
    selfHelpType="generic"
    supportTopicIds="32731224"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Cluster sizing for Hyperscale (Citus)

To size clusters for Hyperscale (Citus), use the following information.

## **Recommended Steps**

* **Multi-tenant SaaS use-case**: 

   * If you're migrating to Citus from an existing single-node database instance, we recommend choosing a cluster where the number of worker cores and RAM in total equals that of the original instance. In this scenario, performance improvements occur because sharding improves resource utilization, allowing for smaller indices.

* **Real-time analytics use-case**: 

   * Total cores: if your working data fits in RAM, you can expect a linear performance improvement on Citus proportional to the number of worker cores. To determine the right number of cores for your needs, consider the current latency for queries in your single-node database and the required latency in Citus. Divide current latency by desired latency, and round the result.

   * Worker RAM: the practice is to provide enough memory so that the majority of the working set fits into the available memory. You can run `EXPLAIN ANALYZE` on a query to determine how much memory it requires.

* A cluster [can be scaled from its initial configuration](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-scaling)
