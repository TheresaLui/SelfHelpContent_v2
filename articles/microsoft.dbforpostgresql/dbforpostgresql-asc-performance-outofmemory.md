<properties
    pageTitle="PostgreSQL server is facing out of memory errors"
    description="PostgreSQL server is facing out of memory errors"
	infoBubbleText="Server is facing out of memory errors. See details on the right"
    service="microsoft.dbforpostgresql"
    resource="dbforpostgresql"
    authors="zhlian"
    ms.author="zhlian"
    displayOrder="100"
	articleId="dbforpostgresql-asc-performance-outofmemory"
	diagnosticScenario="OrcasPostgresOutofMemory"
    selfHelpType="rca"
    supportTopicIds="32639985,32639986,32639987,32640019,32640025,32640026,32640027, 32781006, 32781008, 32781010, 32781012, 32781014"
    resourceTags="windows, linux"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Server is facing out of memory errors

<!--issueDescription-->
The server <!--$ServerName-->ServerName<!--/$ServerName--> has <!--$Count-->Count<!--/$Count--> out of memory errors from <!--$StartTime-->StartTime<!--/$StartTime--> to <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) .
<!--/issueDescription-->

## **Recommended Steps**

* If you have a number of short running queries that run very frequently and perform simple lookups and joins then maintaining a lower *work_mem* is ideal.
* If you need to maintain your current *work_mem* value due to complex queries, consider increasing the amount of overall memory available by scaling up vCores

## **Recommended Documents**

* Review [Configuring memory for Postgres](https://www.citusdata.com/blog/2018/06/12/configuring-work-mem-on-postgres/)<br>
