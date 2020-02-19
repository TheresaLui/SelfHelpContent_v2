<properties
    pageTitle="Orcas MariaDB server is facing high IOPS consumption"
    description="Orcas MariaDB server is facing high IOPS consumption"
    infoBubbleText="Server is facing high IOPS consumption. See details on the right"
    service="microsoft.dbformariadb"
    resource="dbformariadb"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformariadb-asc-performance-highiops"
    diagnosticScenario="OrcasMariaDBHighIOPS"
    selfHelpType="rca"
    resourceTags="servers, databases"
    cloudEnvironments="public"
/>

# Server is facing high IOPS consumption

<!--issueDescription-->
Thank you for contacting Microsoft support about your performance issues with your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that your IOPS consumption was above <!--$IOPercentageThreshold-->IOPercentageThreshold<!--/$IOPercentageThreshold-->% in <!--$Count-->Count<!--/$Count--> instance(s). The longest durations of high io utilization were at: <!--$Periods-->Periods<!--/$Periods-->.
<!--/issueDescription-->

## **Recommended Steps**

Consider increasing [IOPS limits](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers#storage) by scaling storage size. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement.

## **Recommended Documents**

* [Storage IOPS limits](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers#storage)
* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMariaDB)