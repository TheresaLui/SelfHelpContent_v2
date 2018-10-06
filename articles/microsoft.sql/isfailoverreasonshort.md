<properties
	pageTitle="Database connectivity - Failover downtime"
	description="failoverdowntimeshort"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy"
	displayOrder=""
	articleId="FailoverDowntimePlanned_DDE3C31F-19D2-473F-9DDF-5AB905E1F0B0"
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
 
Building in resiliency to your application to account for these situations can help create transparency to the end user when these transient scenarios occur.  The included documentation discusses more information about connectivity in Azure SQL DB, how to implement Retry Logic and common errors in Azure SQL DB. Meanwhile our product team is constantly working to minimize these situations and their impact to your database availability.

<!--/issueDescription-->

