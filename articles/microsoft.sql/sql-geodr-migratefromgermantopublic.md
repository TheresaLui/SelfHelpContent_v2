<properties
	pageTitle="Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure"
	description="Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure"
	service="microsoft.sql"
	resource="servers"
	authors="subbuk"
	authoralias="subbuk"
	ms.author="subbuk"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32785509, 32785645"
	productPesIds="13491, 15660"
	cloudEnvironments="blackForest"
	articleId="427a0459-7468-49d0-9da5-111aa863ecfe"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Geo Replication, Failover Groups and DB Copy/Migration from Microsoft Cloud Germany to global Azure

## **Recommended Steps**

To migrate  smaller Azure SQL database workloads using the offline method, use the export/import method to export your database to a `.bacpac` file and import the `.bacpac` file to the target  server location. You can export and import databases using the Azure portal,  SQLPackage Utility tool, SQL Server Management Studio (SSMS), or PowerShell.

- [Steps to export database to a `.bacpac` file](https://docs.microsoft.com/azure/azure-sql/database/database-export?branch=pr-en-us-138592)<br>
- [Steps to import database from a `.bacpac` file](https://docs.microsoft.com/azure/azure-sql/database/database-import?branch=pr-en-us-138592&tabs=azure-powershell)<br>

### **Migrate using Geo-Replication Method**
Export/import is not recommended for large databases. To migrate a large database, configure active geo-replication from the Azure Germany cloud source, to the Azure Global cloud target. 

To migrate using active geo-replication, provide the required information (as listed in this article) and proceed with creating a support request.
 
**Information required for database migration using active geo-replication**
- Mandatory subscription listing
- Unique pair of  source subscription (Azure Germany subscription) and target subscription ID (Azure Global subscription)
- When submitting support request, provide  Company Name, Name, and Contact Email. Provide the subscriptions in unique pairs, as shown in the following example.

  |No|Azure Germany - source|Azure Global  - target|
  |--|--|--|
  |1 |a312i8348c-dd9f-442c-a531-021090a25833|9909093ce-dd9f-442c-a531-021090a25883|

- If you are migrating databases from, or to, multiple subscriptions, provide unique pairs for allowing active geo-replication migration. The following scenario shows a customer with one Azure Germany subscription who wants to move databases to two different Azure Global subscriptions.

  |No|Azure Germany - source           |Azure Global - target |
  |--|--|--|
  |1 |a312i8348c-dd9f-442c-a531-021090a25833  |9909093ce-dd9f-442c-a531-021090a25883  |
  |2 |a312i8348c-dd9f-442c-a531-021090a25833  |QX3455555e-449f-R23GB-c333-73jdj876eir0  |

- After you receive the access confirmation from us for subscription pairs, follow the instructions to [Migrate your database using active Geo Replication](https://docs.microsoft.com/azure/germany/germany-migration-databases?branch=pr-en-us-138592#migrate-sql-database-using-active-geo-replication)

## **Recommended Documents**

* [Migrate database resources to Azure Global](https://docs.microsoft.com/azure/germany/germany-migration-databases?branch=pr-en-us-138592)<br>
* [Microsoft Cloud Deutschland transition](https://www.microsoft.com/cloud-platform/germany-cloud-regions)   
