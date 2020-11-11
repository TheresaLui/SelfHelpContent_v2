<properties
    pageTitle="PostgreSQL server is facing high IO throttle"
    description="PostgreSQL server is facing high IO throttle"
	infoBubbleText="Server is facing high IO throttle. See details on the right"
    service="microsoft.dbforpostgresql"
    resource="dbforpostgresql"
    authors="danielcarbajal"
    ms.author="dacarbaj"
    displayOrder="100"
	articleId="dbforpostgresql-asc-performance-xiooperation"
	diagnosticScenario="OrcasPostgresXIOThrottle"
    selfHelpType="rca"
    supportTopicIds="32639985,32639986,32639987,32640019,32640025,32640026,32640027, 32781006, 32781008, 32781010, 32781012, 32781014"
    resourceTags="windows, linux"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Server is facing high IO Throttle

<!--issueDescription-->
Thank you for contacting Microsoft support about your performance issues with your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that your IO throttle is above 100 for more than 60 minutes between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. This means there are storage issues.
<!--/issueDescription-->

## **Recommended Steps**

* Consider increasing IOPS by scaling storage size. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement.
* You can also enable [Auto-Grow feature](https://docs.microsoft.com/azure/postgresql/howto-auto-grow-storage-portal), to avoid this issue in the future

## **Recommended Documents**

* [Reaching storage limits](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)
* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforPostgreSQL)
