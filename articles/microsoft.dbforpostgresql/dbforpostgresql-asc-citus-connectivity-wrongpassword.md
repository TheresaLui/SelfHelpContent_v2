<properties
	pageTitle="Login Failed with Wrong Password Entered"
	description="Login failed with wrong password entered"
	infoBubbleText="Found recent connection failure. See details on the right."
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="v-basanj"
	displayOrder=""
	articleId="dbforpostgresql-asc-citus-connectivity-wrongpassword"
	diagnosticScenario="OrcasCitusWrongPasswordInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32639953"
	resourceTags=""
	productPesIds="17068"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforCitus"
/>

# Login failed with wrong password

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed password authentications to Hyperscale (Citus) server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). 
<!--/issueDescription-->

## **Recommended Steps**

* Check the connection string to confirm you have correctly entered the password for this server
* Contact the server's admin to request a password change
