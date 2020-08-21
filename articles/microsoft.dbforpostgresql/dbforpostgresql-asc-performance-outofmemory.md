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
    supportTopicIds="32639985,32639986,32639987,32640019,32640025,32640026,32640027"
    resourceTags="windows, linux"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Server is facing out of memory errors

<!--issueDescription-->
The server <!--$ServerName-->ServerName<!--/$ServerName--> has total <!--$Count-->Count<!--/$Count--> Out of Memory errors from <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) to <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) .
<!--/issueDescription-->

## **Recommended Steps**

* Please suggest customer either to increase the overall RAM on the machine itself by upgrading to a larger instance OR to decrease the amount of memory that *work_mem* uses
* If customers have a number of short running queries that run very frequently and perform simple lookups and joins then maintaining a lower *work_mem* is ideal, in this case customers get diminishing returns by allowing it to be significantly higher because it is simply unused. If workload of customers is relatively few active queries at a time that are doing very complex sorts and joins then granting more memory to prevent things from spilling can give customer great returns.

## **Recommended Documents**

* [Configuring memory for Postgres](https://www.citusdata.com/blog/2018/06/12/configuring-work-mem-on-postgres/)<br>
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforPostgreSQL) <br>
* [Azure Database for PostgreSQL documentation](https://docs.microsoft.com/azure/postgresql/)
