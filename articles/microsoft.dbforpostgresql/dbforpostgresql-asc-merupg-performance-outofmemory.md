<properties
	pageTitle="Server out of memory"
	description="Out of memory errors"
    infoBubbleText="Found recent server errors. See details on the right."
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder=""
	articleId="dbforpostgresql-asc-merupg-performance-outofmemory"
	diagnosticScenario="OrcasMeruPGOutofMemoryInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32628416"
	resourceTags=""
	productPesIds="17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Out of memory

<!--issueDescription-->
There were <!--$Count-->Count<!--/$Count--> out of memory events on PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). 
<!--/issueDescription-->

## Recommended steps

* If there are a number of short running queries that run very frequently and perform simple lookups and joins then maintaining a lower *work_mem* is ideal. If instead the workload has relatively few active queries at a time that are doing very complex sorts and joins then granting more memory to prevent spilling can give great returns.

* Consider scaling up to a compute tier that offers more memory. 

## **Recommended documents**

* [Configuring memory for Postgres](https://www.citusdata.com/blog/2018/06/12/configuring-work-mem-on-postgres/)<br>