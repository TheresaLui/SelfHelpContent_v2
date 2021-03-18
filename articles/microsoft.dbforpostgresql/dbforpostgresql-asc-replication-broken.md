<properties
    pageTitle="PostgreSQL server is facing replication broken issue"
    description="PostgreSQL server is facing replication broken issue"
	infoBubbleText="Server is facing replication broken issue. See details on the right"
    service="microsoft.dbforpostgresql"
    resource="dbforpostgresql"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
	articleId="dbforpostgresql-asc-replication-broken"
	diagnosticScenario="OrcasPostgresReplicationBroken"
    selfHelpType="rca"
    resourceTags="windows, linux"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Broken streaming replication

<!--issueDescription-->
Thank you for contacting Microsoft support about your broken streaming replication issue with your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. Our investigation shows that streaming replication has been broken between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. 
<!--/issueDescription-->

## **Recommended Steps**

1.	Please check if the primary or the replica server has been restarted explicitly or if they have undergone a change in the SKU size, which will also result in a restart. In this case streaming replication will be temporarily broken until both servers are available again. This can also happen for short periods of time during service planned maintenance which happens usually once a month.

2.	If streaming replication is broken for an extended period of time, check connectivity to the primary and the replica servers and if connecitivity failed on one of them please continue filing a support ticket for further investigation.

## **Recommended Documents**

* [Monitoring Replication]( https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#monitor-replication)
* [Planned maintenance notification in Azure Database for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification)
