<properties
	pageTitle="Errors for AWS RDS MySQL to Azure Database for MySQL Online Migration"
	description="Top migration errors and troubleshooting info"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="migration-online-awsrdsmysqltoazuremysql"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32673575"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public"
/>

# Errors you may encounter while migrating from AWS RDS MySQL to Azure Database for MySQL using online migration 

## **Recommended Steps**

**Migration errors - AWS RDS MySQL to Azure Database for MySQL using online migration**

* **Database '{0}' has foreign key(s) on target.** Fix the target and start a new data migration activity. Execute below script on target to list the foreign key(s).

	If you have foreign keys in your schema, the initial load and continuous sync of the migration will fail. Execute the following script in MySQL workbench to extract the drop foreign key script and add foreign key script:

```
SET group_concat_max_len = 8192; SELECT SchemaName, GROUP_CONCAT(DropQuery SEPARATOR ';\n') as DropQuery, GROUP_CONCAT(AddQuery SEPARATOR ';\n') as AddQuery FROM (SELECT KCU.REFERENCED_TABLE_SCHEMA as SchemaName, KCU.TABLE_NAME, KCU.COLUMN_NAME, CONCAT('ALTER TABLE ', KCU.TABLE_NAME, ' DROP FOREIGN KEY ', KCU.CONSTRAINT_NAME) AS DropQuery, CONCAT('ALTER TABLE ', KCU.TABLE_NAME, ' ADD CONSTRAINT ', KCU.CONSTRAINT_NAME, ' FOREIGN KEY (`', KCU.COLUMN_NAME, '`) REFERENCES `', KCU.REFERENCED_TABLE_NAME, '` (`', KCU.REFERENCED_COLUMN_NAME, '`) ON UPDATE ',RC.UPDATE_RULE, ' ON DELETE ',RC.DELETE_RULE) AS AddQuery FROM INFORMATION_SCHEMA.KEY_COLUMN_USAGE KCU, information_schema.REFERENTIAL_CONSTRAINTS RC WHERE KCU.CONSTRAINT_NAME = RC.CONSTRAINT_NAME AND KCU.REFERENCED_TABLE_SCHEMA = RC.UNIQUE_CONSTRAINT_SCHEMA AND KCU.REFERENCED_TABLE_SCHEMA = 'SchemaName') Queries GROUP BY SchemaName;
```

* **Database '{0}' does not exists on server.** Provided MySQL source server is case sensitive. Please check the database name.

	When migrating a MySQL database to Azure using Command Line Interface (CLI), users may hit this error. The service could not locate the database on the source server. This could be because you may have provided incorrect database name or the database does not exist on the listed server. Please note database names are case sensitive. Provide the exact database name to fix the issue.

* **There are tables with the same name in the database '{database}'.** Azure Database for MySQL does not support case sensitive tables.

	This error happens when you have two tables with the same name in the source database. Please note that MySQL database on Azure does not support case sensitive tables. So, update the table names accordingly and try again. 
	
* **The target database {database} is empty.** Please migrate the schema.

	This error occurs when target MySQL database you are migrating to does not have the required schema. Schema migration is required to be able to migrate data to your target. Please [migrate the schema](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#migrate-the-sample-schema) from your source to the target database.
	
## **Recommended Documents**

* [Tutorial: Migrate MySQL to Azure Database for MySQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online)<br>
* [Azure Database for MySQL Documentation](https://docs.microsoft.com/azure/mysql)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)
