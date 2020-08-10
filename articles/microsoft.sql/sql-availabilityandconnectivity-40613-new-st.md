<properties
    pageTitle="Database X on server Y is not currently available"
    description="Database X on server Y is not currently available"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745430"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="E8D094DB-9BC4-40D3-8C7A-41CD46189C84"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Database X on server Y is not currently available

## **Recommended Steps**

Error 40613 is a nonspecific, [transient error](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745425) that is returned when your database is unavailable.  It is nonspecific because it is returned for all types of unavailability, including:
 - **User-initiated action** - certain operations that change the database configuration may briefly make the database unavailable.  Some of the most common are [scaling the database](https://docs.microsoft.com/azure/azure-sql/database/single-database-scale?WT.mc_id=pid:13491:sid:32745425#impact) or [elastic pool](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-scale?WT.mc_id=pid:13491:sid:32745425#impact-of-changing-service-tier-or-rescaling-compute-size)
 - **Planned maintenance** - the service periodically performs [planned maintenance](https://docs.microsoft.com/azure/azure-sql/database/planned-maintenance?WT.mc_id=pid:13491:sid:32745425) to deploy software upgrades and other system enhancements.  This usually occurs less than twice a month.
 - **Unplanned failover** - unexpected events such as a software crash, hardware failure, etc.

During the period the service is reconfiguring your database on different hardware, all attempts to connect to the database will receive error 40613.  The [Resource Health events](https://docs.microsoft.com/azure/azure-sql/database/resource-health-to-troubleshoot-connectivity?WT.mc_id=pid:13491:sid:32745425) will reflect that the database was unavailable within 15 minutes.  If a more detailed unavailability reason is available, resource health is updated with this information, usually within 30 minutes.

To resolve this issue:
1. Check Resource Health to see whether there is a detailed unavailability reason, and whether it is being caused by a user-initiated action.  If so, try to schedule these operations during a time that reduces impact.  
2. Make sure that all production applications have robust [retry logic](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745425#retry-logic-for-transient-errors).  Most database unavailability is brief, so retry logic may allow the operation to complete successfully.
3. Subscribe to planned maintenance notifications.
4. Contact Azure Support for assistance with unplanned failovers or extended database unavailability.