<properties
    pageTitle="Scaling a geo-replicated instance"
    description="Scaling a geo-replicated instance"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32748012"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags=""
    articleId="sqlmi-failovergroups-scaling"
    ownershipId="AzureData_AzureSQLMI"
/>

# Scaling a geo-replicated instance

You can upgrade or downgrade a primary managed instance to a different compute size (within the same service tier, not between General Purpose and Business Critical) without disconnecting the failover group.  

## **Recommended Steps**

- When upgrading, we recommend that you upgrade the secondary instance first, and then upgrade the primary
- When downgrading, reverse the order: downgrade the primary first, and then downgrade the secondary

This sequence is recommended specifically to avoid the problem where the secondary at a lower SKU gets overloaded and must be re-seeded during an upgrade or downgrade process. You could also avoid the problem by making the primary read-only, at the expense of impacting all read-write workloads against the primary.

- It is not recommended to downgrade the secondary instance, this is to ensure your data tier has sufficient capacity to process your regular workload after failover is activated
