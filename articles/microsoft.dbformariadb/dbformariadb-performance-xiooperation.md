<properties
    pageTitle="Orcas Mariadb server is facing high IO throttle"
    description="Orcas Mariadb server is facing high IO throttle"
    infoBubbleText="Server is facing high IO throttle. See details on the right"
    service="microsoft.dbformariadb"
    resource="dbformariadb"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformariadb-performance-xiooperation"
    diagnosticScenario="OrcasMariadbXIOThrottle"
    selfHelpType="rca"
    resourceTags="servers, databases"
    cloudEnvironments="public"
/>

# Server is facing high IO Throttle

<!--issueDescription-->
Thank you for contacting Microsoft support about your performance issues with your Mariadb server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that your IO throttle is above 100 for more than 60 minutes between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. This means there are storage issues.
<!--/issueDescription-->

## **Recommended Steps**

* Consider increasing IOPS by scaling storage size. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement.
* You can also enable [Auto-Grow feature](https://docs.microsoft.com/azure/mariadb/howto-auto-grow-storage-portal), to avoid this issue in the future.

## **Recommended Documents**

* [Performance Recommendations in Azure Database for Mariadb](https://docs.microsoft.com/en-us/azure/mariadb/concepts-performance-recommendations)<br>
* [Troubleshoot common connectivity issues to Azure Databases for Mariadb](https://docs.microsoft.com/en-us/azure/mariadb/howto-troubleshoot-common-connection-issues)
* [Query Performance Insight in Azure Database for Mariadb](https://docs.microsoft.com/en-us/azure/mariadb/concepts-query-performance-insight)
* [Azure Database for Mariadb documentation](https://docs.microsoft.com/azure/mariadb/)