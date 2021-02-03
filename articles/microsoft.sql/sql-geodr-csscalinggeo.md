<properties
	pageTitle="Geo Replication, Failover Groups and DB Copy/Scaling a geo-replicated database"
	description="Geo Replication, Failover Groups and DB Copy/Scaling a geo-replicated database"
	service="microsoft.sql"
	resource="servers"
	authors="subbuk,maboja-msft"
	ms.author="subbuk,maboja"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32731233"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="f96fe5cd-007c-4453-b4a2-00dbd693ef2b"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Scaling a Geo Replicated Database

## **Recommended Steps**

### Scaling Geo Replicated database

* You can upgrade or downgrade a primary database i to a different compute size (within the same service tier, not between General Purpose and Business Critical) without disconnecting any secondary databases
* When upgrading, we recommend that you upgrade the secondary database first, and then upgrade the primary
* When downgrading, reverse the order: downgrade the primary first, and then downgrade the secondary. When you upgrade or downgrade the database to a different service tier, this recommendation is enforced.
* The primary database in a failover group can't scale to a higher tier unless the secondary database is first scaled to the higher tier. If you try to scale the primary database before the secondary database is scaled, you might receive the error:  *The source database 'Primaryserver.DBName' cannot have higher edition than the target database 'Secondaryserver.DBName'. Upgrade the edition on the target before upgrading the source.*

**Scaling geo secondary database that is part of Failover Group**

* If you created secondary database as part of the failover group configuration it is not recommended to downgrade the secondary database. This is to ensure your data tier has sufficient capacity to process your regular workload after failover is activate.

## **Recommended Documents**

* [Scaling Geo Database](https://docs.microsoft.com/azure/sql-database/sql-database-active-geo-replication?WT.mc_id=pid:13491:sid:32731233/#upgrading-or-downgrading-primary-database)<br>
* [Configuring geo Secondary](https://docs.microsoft.com/azure/sql-database/sql-database-active-geo-replication?WT.mc_id=pid:13491:sid:32731233/#configuring-secondary-database)<br>
