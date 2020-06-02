<properties
	pageTitle="Connection Token Invalid"
	description="Connection Token Invalid"
	infoBubbleText="AAD Connection Token Invalid"
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy, swbhartims"
	ms.author="subbuk, swbharti"
	displayOrder=""
	articleId="IsTokenNotValid_95889E41-4BCE-4142-994B-FF931D177FEA"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="31980414"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC, connections to server <!--$ServerName-->ServerName<!--/$ServerName--> and database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> were denied due to an invalid AAD token. Token expiry is the most common cause for token to become invalid. By default, the connection token is valid for one hour. Please ensure to use a valid token to connect to your database successfully. This issue may also occur if any of the registered claims in the identity(ID) token is invalid. Please review the documents below for more information.
<!--/issueDescription-->

## **Recommended Documents**

* [Obtaining Azure Active Director (AAD) Connection token](https://blogs.technet.microsoft.com/stefan_stranger/2018/06/06/connect-to-azure-sql-database-by-obtaining-a-token-from-azure-active-directory-aad/)
* [Understanding JWT identity Claims for AAD Connection Token](https://docs.microsoft.com/azure/architecture/multitenant-identity/claims)
