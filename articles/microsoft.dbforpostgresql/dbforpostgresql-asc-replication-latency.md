<properties
    pageTitle="PostgreSQL server is facing high replication latency issue"
    description="PostgreSQL server is facing high replication latency issue"
	infoBubbleText="Server is facing high replication latency issue. See details on the right"
    service="microsoft.dbforpostgresql"
    resource="dbforpostgresql"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
	articleId="dbforpostgresql-asc-replication-latency"
	diagnosticScenario="OrcasPostgresReplicationLAtency"
    selfHelpType="rca"
    resourceTags="windows, linux"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# High replication latency

<!--issueDescription-->
Thank you for contacting Microsoft support about your replication latency issues with your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation showed that replication lag has been greater than <!--$LATENCY_THRESHOLD-->LATENCY_THRESHOLD<!--/$LATENCY_THRESHOLD--> between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. 
<!--/issueDescription-->

## **Recommended Steps**

1.	Please check if there is any write activity on the primary server. Please note that the absence of any write activity on the primary server can cause the latency to show as high as 300s on basic servers or 900s on General Purpose/Memory Optimized servers. If you see this pattern, this is not a real latency. In this case checking the lag_in_bytes metric on the primary server usually shows a value of 0, which means there is no real data lag. The lag_in_seconds is only meaningful when there is constant write activity on the primary.

2.	Please check if the latency is regularly going beyond the threshold. If so the primary might be having heavy write workload at regular intervals. To decrease the replica lag consider increasing the vcores on the replica server. 

## **Recommended Documents**

* [Monitoring Replication]( https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#monitor-replication)

