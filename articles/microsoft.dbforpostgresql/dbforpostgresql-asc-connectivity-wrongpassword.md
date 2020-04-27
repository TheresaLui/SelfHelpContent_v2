<properties
	pageTitle="Login Failed with Wrong Password Entered"
	description="RCA - Login Failed with Wrong Password Entered RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="zhlian"
	ms.author="zhlian"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-wrongpassword"
	diagnosticScenario="OrcasPostgresWrongPasswordInsightV2TroubleShooter"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect to Postgres server: incorrect password

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed password authentications to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). 
<!--/issueDescription-->

## **Recommended Steps**

* Check the connection string to confirm you have correctly entered the password for this server
* Consider changing the password and reattempting to connect using the new password

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
