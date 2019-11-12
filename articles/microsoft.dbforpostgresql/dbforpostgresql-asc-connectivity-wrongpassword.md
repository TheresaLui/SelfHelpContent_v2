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
	cloudEnvironments="public"
/>
# Can't connect PostgreSQL database server because wrong password entered

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that <!--$Count-->Count<!--/$Count--> connection attempts to fail due to wrong password entered between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. Please review the activity logs in the portal to see the password change history if the change made by you. If you keep seeing the errors, please consider resetting the password and retry the connection using the most updated password.
<!--/issueDescription-->

## **Recommended Steps**

* Please make sure to use the most updated password to log in

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
