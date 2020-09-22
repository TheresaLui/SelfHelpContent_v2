<properties
    pageTitle="Orcas MariaDB server is facing high IO throttle"
    description="Orcas MariaDB server is facing high IO throttle"
    infoBubbleText="Server is facing high IO throttle. See details on the right"
    service="microsoft.dbformariadb"
    resource="dbformariadb"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformariadb-asc-performance-xiooperation"
    diagnosticScenario="OrcasMariaDBXIOThrottle"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Server is facing high IO Throttle

<!--issueDescription-->
During our investigation regarding performance issues to your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> we found that your IO throttle is above 100 for more than 60 minutes between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). This means there are storage issues.
<!--/issueDescription-->

## **Recommended Steps**

* Consider increasing IOPS by scaling storage size. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement.
* You can also enable [Auto-Grow feature](https://docs.microsoft.com/azure/mariadb/howto-auto-grow-storage-portal), to avoid this issue in the future.

## **Recommended Documents**

* [Reaching storage limits](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers)
* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMariaDB)