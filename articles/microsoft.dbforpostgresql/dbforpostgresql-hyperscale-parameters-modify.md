<properties
    pageTitle="Modify parameters in Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Modify parameters in Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource=""
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-parameters-modify.md"
    selfHelpType="generic"
    supportTopicIds="32639997, 32640021"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Modify configuration parameters

In the Azure portal page for your Hyperscale (Citus) server group, you can view and update *Coordinator node parameters* or *Worker node parameters*. Changes to *Worker node parameters* will apply to all worker nodes.

## **Recommended Steps**
* Parameters that are not listed in the Azure portal are not available for reconfiguration. This includes `max_connections`; learn more about [connection limits](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-configuration-options#limits-and-limitations).
* Submit requests or vote on [our feedback page](https://feedback.azure.com/forums/597976-azure-database-for-postgresql) for parameters you would like supported

## **Recommended Documents**

* [High availability in Hyperscale (Citus)](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-high-availability)
* [Available extensions Hyperscale (Citus)](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-extensions)
