<properties
    pageTitle="Orcas MySQL server is facing high IOPS consumption"
    description="Orcas MySQL server is facing high IOPS consumption"
    infoBubbleText="Server is facing high IOPS consumption. See details on the right"
    service="microsoft.dbformysql"
    resource="dbformysql"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformysql-asc-performance-highiops"
    diagnosticScenario="OrcasMySQLHighIOPS"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Server is facing high IOPS consumption

<!--issueDescription-->
During our investigation regarding performance issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName--> we found that your IOPS consumption was above <!--$IOPercentageThreshold-->IOPercentageThreshold<!--/$IOPercentageThreshold-->% in <!--$Count-->Count<!--/$Count--> instance(s). The longest durations (UTC) of high IOPS consumption were at: <!--$Periods-->Periods<!--/$Periods-->.
<!--/issueDescription-->

## **Recommended Steps**

Consider increasing [IOPS limits](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#storage) by scaling storage size. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement.


## **Recommended Documents**

* [Storage IOPS limits](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#storage)
* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)