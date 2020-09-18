<properties
	pageTitle="Business Continuity|How to questions or planning a recovery strategy"
	description="Business Continuity|How to questions or planning a recovery strategy"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637266"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="de6cd457-a03a-4c2d-9a1b-18940b998243"
	ownershipId="AzureData_AzureSQLMI"
/>

# Planning a recovery strategy

## **Recommended Steps**

SQL Database Managed Instance provides several business continuity features, including automated backups and optional database replication that can mitigate service disruption scenarios. First, you need to understand how SQL Database [high availability architecture](https://docs.microsoft.com/azure/sql-database/sql-database-high-availability) provides 99.99% availability and resiliency to some disruptive events that might affect your business process. Then, you can learn about the additional mechanisms that you can use to recover from the disruptive events that cannot be handled by SQL Database high availability architecture, listed below.

Each mechanism has different characteristics for estimated recovery time (ERT) and potential data loss for recent transactions. Once you understand these options, you can choose among them - and, in most scenarios, use them together for different scenarios. As you develop your business continuity plan, you need to understand the maximum acceptable time before the application fully recovers after the disruptive event. The time required for application to fully recover is known as recovery time objective (RTO). You also need to understand the maximum period of recent data updates (time interval) the application can tolerate losing when recovering after the disruptive event. The time period of updates that you might afford to lose is known as recovery point objective (RPO).

## **Recommended Documents**

- [Overview of business continuity with Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-business-continuity)
- [Temporal tables](https://docs.microsoft.com/azure/sql-database/sql-database-temporal-tables) enable you to restore row versions from any point in time.
- [Built-in automated backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) and [Point in Time Restore](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups#point-in-time-restore) enable you to restore complete database to some point in time within the last 35 days.
- You can [restore a deleted database](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Restore-dropped-database-on-Azure-SQL-Managed-Instance/ba-p/386285) to the point at which it was deleted.
- Active geo-replication enables you to create readable replicas and manually failover to any replica in case of a data center outage or application upgrade.
- Use [geo-redundant database backups](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups#geo-restore) (geo-restore) to restore a database in any Azure region.
- [Auto-failover group](https://docs.microsoft.com/azure/sql-database/sql-database-auto-failover-group#best-practices-of-using-failover-groups-with-managed-instances) allows the application to automatically recover in case of a data center outage.