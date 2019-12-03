<properties
	pageTitle="Managed Instance - Plan cache defect"
	description="Managed Instance - Plan cache defect"
	infoBubbleText="Managed Instance was facing performance degradation due to defect in plan cache."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="zlradeti"
	authors="zlradeti"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_PlanCacheDefect"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	articleId="sqlmanagedinstance-perf-plan-cache-defect"
/>

# Managed Instance - Plan cache defect

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup-->  had degraded performance between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> due to defect in plan cache.

SQL Managed Instance team recently detected a defect in plan caching logic for internal, system queries which causes plans for internal queries to pile up and deteriorate caching performance over time for Bound Trees, Object Plans and SQL Plans cache stores. According to the spinlock stats and high query compile CPU time that we noticed on your instance, there is a big  chance that this plan cache defect is a root cause of the performance degradation you are facing. 

Engineers are working on a fix for this issue and it will be deployed with the next release cycle of Managed Instance.

<!--/issueDescription-->

## Recommended Steps

To mitigate the issue with minimal impact to your workload, we propose creating a periodic task that would cleanup internal plans from abovementioned caches.

This can be achieved through scheduled SQL Agent job and using the following DBCC commands:	 

- dbcc freesystemcache('Bound Trees', internal) 
- dbcc freesystemcache('Object Plans', internal)  	
- dbcc freesystemcache('SQL Plans', internal) 

__If you apply this mitigation please contact <clperfdevs@service.microsoft.com> so we could let you know when the fix is deployed and SQL Agent job can be turned off.__