<properties
    pageTitle="Error 40613: Database x on server y is not currently available"
    description="Error 40613: Database x on server y is not currently available"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32746125"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags=""
    articleId="sqlmi-conn-ts-40613"
    ownershipId="AzureData_AzureSQLMI"
/>

# Database X on server Y is not currently available

**Error 40613: Database {databasename} on server {servername} is not currently available.**

Error 40613 is a nonspecific, [transient error](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues) returned by Azure any time your database is unavailable. The common types of unavailability are caused by:

 - **User-initiated actions**: certain operations that change the database configuration may briefly make the database unavailable, the most common is scaling an instance.
 - **Planned maintenance**: the service periodically performs [planned maintenance](https://docs.microsoft.com/azure/azure-sql/database/planned-maintenance) to deploy software upgrades and other system enhancements. This usually occurs less than twice a month.
 - **Unplanned failover**: unexpected events such as a software crash, hardware failure, etc.

During the period the service is reconfiguring your primary database replica, attempts to connect to the database will fail with error 40613.

## **Recommended Steps**

1. You should expect occasional, brief windows (e.g., less than 60 seconds) where you see error 40613. Make sure that all production applications have robust [retry logic](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors) to handle this.
1. Contact Azure Support if you need assistance with periods of extended database unavailability
