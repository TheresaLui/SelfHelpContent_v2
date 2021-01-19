<properties
    pageTitle="Lag on geo-secondary instance"
    description="Lag on geo-secondary instance"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32748011"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags=""
    articleId="sqlmi-failovergroups-lag"
    ownershipId="AzureData_AzureSQLMI"
/>

# Lag on geo-secondary instance

Replication lag on secondary can occur due to combination of a heavy write workload on the Primary and imbalance between the service objective of Geo-Primary and Geo-Secondary where Geo-Secondary unable to keep up.

## **Recommended Steps**

- If you have a largely different service-objective between primary and secondary, upgrade the Geo-Secondary to the same service-objective as the Geo-Primary is recommended

## **Recommended Documents**

[Monitoring geo replication lag](https://docs.microsoft.com/azure/azure-sql/database/active-geo-replication-overview#monitoring-geo-replication-lag)
