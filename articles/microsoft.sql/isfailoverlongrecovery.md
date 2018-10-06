<properties
	pageTitle="Database connectivity - Failover downtime LongRecovery"
	description="failoverlongrecovery"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy"
	displayOrder=""
	articleId="PlanedFailoverLR_1FBC4A97-DC3A-4DF9-86C0-46B00AF0F733"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds="31980414"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between {StartTime} and {EndTime} the database {DatabaseName} on server {ServerName} experienced {FailoverCount} reconfiguration(s). The total time of unavailability caused by these reconfiguration(s) was {FailoverTotalSeconds} seconds.  
 
The Azure infrastructure has the ability to dynamically reconfigure servers for planned operations such as load balancing and updates or unplanned occurrences such as health recoveries from software or hardware issues. In this scenario this was due to planned operation(s) specifically related to {FailoverPlannedReason}.  In general, reconfigurations are short in duration and below 60 seconds.  
 
In this scenario, the large part of the reconfiguration duration totaling {RecoveryDuration} seconds was due to a long recovery of transactions that were running on the database at the time of the reconfiguration.  As Azure SQL Databases need to maintain transactional consistency, transactions that are in flight during this operation will need to roll back and if large in size can take a longer time to complete.  While this is expected behavior, implementing best practices such as batching transactions to smaller sizes will result in less recovery time when these operations will occur. 
 
In addition, building in resiliency to your application to account for these situations can help create transparency to the end user when these transient scenarios occur.  The included documentation discusses more information about connectivity in Azure SQL DB, how to implement Retry Logic, common errors in Azure SQL DB and discussions on batching in Azure SQL DB. Meanwhile our product team is constantly working to minimize these situations and their impact to your database availability.

<!--/issueDescription-->

