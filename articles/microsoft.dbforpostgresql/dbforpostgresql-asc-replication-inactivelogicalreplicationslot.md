<properties
	pageTitle="Inactive logical replication slot in Azure Database for PostgreSQL"
	description="Inactive logical replication slot in Azure Database for PostgreSQL"
	infoBubbleText="Inactive logical replication slot detected"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder="100"
	articleId="dbforpostgresql-asc-replication-inactivelogicalreplicationslot"
	diagnosticScenario="OrcasPostgresInactiveLogicalReplicationSlotV2TroubleShooter"
	selfHelpType="diagnostics"
	supportTopicIds="32639973, 32639976, 32639992, 32639995, 32640026, 32731228, 32639968, 32639994"
	cloudEnvironments="public, blackForest, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

Our telemetry has alerted us to an inactive logical replication slot (<!--$Slotname --> Slotname <!--/$Slotname -->) on your Azure Database for PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->.
A replication slot that is not consumed causes your server storage to fill up. When storage is almost full, your server will become read-only. In extreme cases, unconsumed slots can lead to transaction ID wraparound. 

## **Recommended Steps**

* If the slot is no longer needed, delete it using the following command:
`SELECT pg_drop_replication_slot('<slotname>');`

* Start consuming the data from the logical replication slot

* If you are not ready to use the replication slot, consider dropping the slot now and creating it when your application is ready to start consuming it

* [Configure an alert](https://docs.microsoft.com/azure/postgresql/howto-alert-on-metric) for your storage usage metric to help monitor growth 
  

## **Recommended Documents**
* Official PostgreSQL documentation [cautions about inactive replication slots](https://www.postgresql.org/docs/current/logicaldecoding-explanation.html)
* [Logical decoding blog](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/change-data-capture-in-postgres-how-to-use-logical-decoding-and/ba-p/1396421)
