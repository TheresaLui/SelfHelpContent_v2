<properties
	pageTitle="Logins temporarily locked out"
	description="Insight to determine the cause of the temporary lock out of logins"
	infoBubbleText="Found that some of the logins were temporarily locked out."
	service="microsoft.sql"
	resource="servers"
	authors="VMMicrosoft"
	ms.author="vimahadi"
	displayOrder=""
	articleId="HasDoSGuardTriggered_1F33F35F-FB10-4E34-89B6-25BEFA276D9A-new-st"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="31980414,32745423"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC, the logins to database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->** were temporarily locked out due to multiple failed logins trying to connect to the server.

The login failures occurred possibly due to one or more of the following reasons below.
<!--/issueDescription-->

### **Possible Reasons for Failure**
<!--$CustomerErrorList-->CustomerErrorList<!--/$CustomerErrorList-->
