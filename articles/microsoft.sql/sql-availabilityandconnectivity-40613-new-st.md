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

Error 40613 is a nonspecific, [transient error](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745425) returned by Azure when your database is unavailable.  It is returned for all types of unavailability, including:
 - **User-initiated actions** - certain operations that change the database configuration may briefly make the database unavailable.  Some of the most common are [scaling the database](https://docs.microsoft.com/azure/azure-sql/database/single-database-scale?WT.mc_id=pid:13491:sid:32745425#impact) or [elastic pool](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-scale?WT.mc_id=pid:13491:sid:32745425#impact-of-changing-service-tier-or-rescaling-compute-size)
 - **Planned maintenance** - the service periodically performs [planned maintenance](https://docs.microsoft.com/azure/azure-sql/database/planned-maintenance?WT.mc_id=pid:13491:sid:32745425) to deploy software upgrades and other system enhancements.  This usually occurs less than twice a month.
 - **Unplanned failover** - unexpected events such as a software crash, hardware failure, etc.

During the period the service is reconfiguring your primary database replica to a new location, all attempts to connect to the database will fail with error 40613.  Within 15 minutes, [Resource Health](https://docs.microsoft.com/azure/azure-sql/database/resource-health-to-troubleshoot-connectivity?WT.mc_id=pid:13491:sid:32745425) events will reflect that the database was unavailable.  If a more detailed unavailability reason is available, Resource Health is updated with this information, usually within 30 minutes.

To resolve this issue:
1. You should expect periodic, brief windows (e.g., less than 60 seconds) where you see this error.  Make sure that all production applications have robust [retry logic](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745425#retry-logic-for-transient-errors) to handle this.
1. Check Resource Health to see whether there is a detailed unavailability reason, and whether it is being caused by a user-initiated action.  If so, schedule these operations during a time that reduces impact.  
1. Subscribe to planned maintenance notifications.  <how to do this goes here>
1. Contact Azure Support if you need assistance with unplanned failovers or periods of extended database unavailability from other causes.