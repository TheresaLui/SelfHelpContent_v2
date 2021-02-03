 
<properties
pageTitle="Database X on server Y is not currently available"
description="Database X on server Y is not currently available"
ms.author="vimahadi"
displayOrder=""
articleId="9177ad6f-bed8-4e86-937f-0189ce40b3a3"
selfHelpType="Apollo"
supportTopicIds="278a9b19-4bb9-af84-f8b6-ec40601d9a5e"
productPesIds="13491"
cloudEnvironments="public"
ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Troubleshooting SQL Db connectivity error 40613 
 
:::Section Insights:::
## Troubleshooting SQL Db connectivity error 40613 
Get help from SQL Db diagnostics and recommended troubleshooting steps below to resolve SQL Db connectivity error 40613.

### SQL Db connectivity diagnostics

<Insight>
    <symptomId>SqlLts,SqlCustomerVerbatims,SqlConnectivity,SqlConnectivityBasic</symptomId>
    <executionText>The diagnostic is running some checks on your resource</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText> 
    <noResultText>The diagnostic did not find any issues. Use the troubleshooting steps below to resolve your problem</noResultText>
    <additionalInputsReq>true</additionalInputsReq> 
    <maxInsightCount>2</maxInsightCount>
</Insight>

### Troubleshooting Error 40613

Error 40613 is a nonspecific, [transient error](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745430) returned by Azure any time your database is unavailable. The common types of unavailability are caused by:

 - **User-initiated actions**: certain operations that change the database configuration may briefly make the database unavailable. Some of the most common are [scaling the database](https://docs.microsoft.com/azure/azure-sql/database/single-database-scale?WT.mc_id=pid:13491:sid:32745425#impact) or [elastic pool](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-scale?WT.mc_id=pid:13491:sid:32745430#impact-of-changing-service-tier-or-rescaling-compute-size).
 - **Planned maintenance**: the service periodically performs [planned maintenance](https://docs.microsoft.com/azure/azure-sql/database/planned-maintenance?WT.mc_id=pid:13491:sid:32745430) to deploy software upgrades and other system enhancements. This usually occurs less than twice a month.
 - **Unplanned failover**: unexpected events such as a software crash, hardware failure, and so on.

During the period the service is reconfiguring your primary database replica, attempts to connect to the database will fail with error 40613. Within a few minutes (needed to process the health signal), [Resource Health](https://docs.microsoft.com/azure/azure-sql/database/resource-health-to-troubleshoot-connectivity?WT.mc_id=pid:13491:sid:32745430) should reflect that the database is unavailable. As additional telemetry becomes available, analysis is performed to determine the detailed cause of unavailability. Resource Health is updated with the detailed unavailability reason (when available) in about two and a half hours.

### Additional recommendations

1. You should expect occasional, brief windows (e.g., less than 60 seconds) where you see error 40613. Make sure that all production applications have robust [retry logic](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745430#retry-logic-for-transient-errors) to handle this.
1. Check Resource Health to see whether there is a detailed unavailability reason, and whether it is being caused by a user-initiated action. If so, schedule these operations during a time that reduces impact. 
1. Subscribe to planned maintenance notifications in [Azure Service Health](https://docs.microsoft.com/azure/service-health/service-health-overview?WT.mc_id=pid:13491:sid:32745430), so you know when planned maintenance activities will occur and can set expectations with your users
1. Contact Azure Support if you need assistance with unplanned failovers or periods of extended database unavailability from other causes
