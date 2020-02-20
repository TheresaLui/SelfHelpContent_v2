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
	productPesIds="16222"
	cloudEnvironments="public, blackForest, fairfax, mooncake"
/>
# Can't connect to Postgres server: incorrect password

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. We found that there have been <!--$Count-->Count<!--/$Count--> failed connection attempts between <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC) due to incorrect password errors. 
<!--/issueDescription-->

## **Recommended Steps**

1. Check the connection string to confirm you have correctly entered the password for this server
2. Consider changing the password and reattempting to connect using the new password

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
