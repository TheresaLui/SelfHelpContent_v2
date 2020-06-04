<properties
	pageTitle="Login Failed with Wrong Password Entered"
	description="Login failed with wrong password entered"
	infoBubbleText="Found recent connection failure. See details on the right."
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder=""
	articleId="dbforpostgresql-asc-merupg-connectivity-wrongpassword"
	diagnosticScenario="OrcasMeruPGWrongPasswordInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32639953"
	resourceTags=""
	productPesIds="17069"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Login failed with wrong password

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed password authentications to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). 
<!--/issueDescription-->

## **Recommended Steps**

* Check the connection string to confirm you have correctly entered the password for this server
* Contact the server's admin to request a password change