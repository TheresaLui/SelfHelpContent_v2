<properties
	pageTitle="Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure"
	description="Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure"
	service="microsoft.sql"
	resource="servers"
	authors="subbuk"
	ms.author="subbuk"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32785509"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="427a0459-7468-49d0-9da5-111aa863ecfe"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure

## **Recommended Steps**

To migrate  smaller Azure SQL database workloads using offline method, you can use export/import method to export your database to  .bacpac and import the .bacpac to the target  server location. Exporting and Importing azure database can be done using Azure Portal,  SQLPackage Utility tool, SQL Server Management Studio (SSMS) and PowerShell.

- [Steps to Export Database to a .bacpac](https://docs.microsoft.com/azure/azure-sql/database/database-export?branch=pr-en-us-138592)<br>


- [Steps to Import database from a .bacpac](https://docs.microsoft.com/azure/azure-sql/database/database-import?branch=pr-en-us-138592&tabs=azure-powershell)<br>


### **Migrate database using Geo-Replication Method**
For large database it is not recommended using export/import method. To migrate large database you can configure active geo-replication from Azure Germany Cloud(Source) to Global Azure cloud (Target)

If you prefer to migrate using Active Geo-Replication, please follow the instructions below and then proceed with creating a support request to get required access for your subscriptions.

**Requirements**
- Mandatory subscription listing is required for the database migration using active geo-replication from Microsoft Cloud Germany (MCG) to Azure Global Cloud (AGC).
- Unique pair of your  Source Subscription (Germany Cloud Subscription) and target subscription ID (Global Azure Subscription) is required  to allow active geo-replication for  database migration from German cloud to Global azure subscription.
- When submitting this request, please ensure to provide  Company Name, Name, Contact Email and list the subscriptions in unique pairs  as shown below.

- |No|Microsoft Cloud Germany (MCG)- source           |Azure Global Cloud (AGC)- target |
|--|--|--|
|1 |a312i8348c-dd9f-442c-a531-021090a25833  |9909093ce-dd9f-442c-a531-021090a25883  |

- For customers with either multiple  Source Or multiple Target subscription(s), please ensure to provide  unique pairs for allowing Active Geo-Replication Migration. Sample scenario below showing, customer with 1 German cloud subscription want to move databases to two different Azure Global subscription.

 |No|Microsoft Cloud Germany (MCG)- source           |Azure Global Cloud (AGC)- target |
|--|--|--|
|1 |a312i8348c-dd9f-442c-a531-021090a25833  |9909093ce-dd9f-442c-a531-021090a25883  |
|2 |a312i8348c-dd9f-442c-a531-021090a25833  |QX3455555e-449f-R23GB-c333-73jdj876eir0  |

- Once you receive the access confirmation from us for subscription pairs, please  follow the instructions to [Migrate your database using active Geo Replication](https://docs.microsoft.com/azure/germany/germany-migration-databases?branch=pr-en-us-138592#migrate-sql-database-using-active-geo-replication)


## **Recommended Documents**

* [Migrate database resources to Global Azure](https://docs.microsoft.com/azure/germany/germany-migration-databases?branch=pr-en-us-138592)<br>
* [Microsoft Cloud Deutschland transition](https://www.microsoft.com/cloud-platform/germany-cloud-regions)   
