<properties
    pageTitle="Orcas PostgreSQL server is facing high IO throttle"
    description="Orcas PostgreSQL server is facing high IO throttle"
	infoBubbleText="Server is facing high IO throttle. See details on the right"
    service="microsoft.dbforpostgresql"
    resource="dbforpostgresql"
    authors="danielcarbajal"
    ms.author="dacarbaj"
    displayOrder="100"
	articleId="dbforpostgresql-asc-performance-xiooperation"
	diagnosticScenario="OrcasPostgresXIOThrottle"
    selfHelpType="rca"
    supportTopicIds="32640027"
    resourceTags="windows, linux"
    productPesIds="16222"
    cloudEnvironments="public"
/>

# Server is facing high IO Throttle

<!--issueDescription-->
Thank you for contacting Microsoft support about your performance issues with your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that your IO throttle is above 100 for more than 60 minutes between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. This means there are storage issues.
<!--/issueDescription-->

## **Recommended Steps**

* Consider increasing IOPS by scaling storage size.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforPostgreSQL)