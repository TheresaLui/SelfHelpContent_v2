<properties
    pageTitle="Database Resource Limits Hit"
    description="Sub Core Database Resource Limits Hit"
    infoBubbleText="The resource limits were hit for this database. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="ketho00"
    ms.author="ketho"
    displayOrder=""
    articleId="Subcore_166C42B9-A932-407E-A9AE-4B454D7986BF"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32749513,32749514,32749515,32749520,32749526"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Database Resource Limits Hit  

<!--issueDescription-->
We detected that your database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->** hit resource limits in **<!--$Resources-->Resources<!--/$Resources-->** between **<!--$CustomizedStartTime-->CustomizedStartTime<!--/$CustomizedStartTime-->** and **<!--$CustomizedEndTime-->CustomizedEndTime<!--/$CustomizedEndTime-->**. This database is using service tier **<!--$Slo-->Slo<!--/$Slo-->**, which provides less than one vCore of CPU.  
<!--/issueDescription-->

Due to the limits being reached, you can face the following issues:  

* Database Availability/Connectivity Issues (Error 40613): Reaching resource limits on databases with less than one vCore of CPU can cause Out of Memory issues which are often accompanied by severe performance issues. These other performance issues can trigger failover and cause unavailability.   
* Metrics Missing: The database may remain active, but you may see metrics missing from Azure Portal due to lack of available memory for telemetry processes.
* Performance Issues: Reaching resource limits may impact the overall performance of the database and cause query slowness and timeouts.

## **Recommended Steps**

To improve performance, consider the following recommendations:   

* [Upgrade the database to a higher service tier](https://docs.microsoft.com/azure/azure-sql/database/purchasing-models)
    * If you are unable to scale-up, we recommend you first reduce the workload and then try again to scale-up the database
* Tune the top resource-consuming queries using [Query Performance Insights](https://docs.microsoft.com/azure/azure-sql/database/query-performance-insight-use)
* Reduce workload demands on the database
