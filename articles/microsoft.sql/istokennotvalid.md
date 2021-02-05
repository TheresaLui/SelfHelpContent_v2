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
	diagnosticScenario="SqlConnectivity"
	selfHelpType="rca"
	supportTopicIds="31980414"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Connectivity"
/>
# Connection token invalid

## **Connections denied due to an invalid AAD token**

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC, connections to server <!--$ServerName-->ServerName<!--/$ServerName--> and database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> were denied due to an invalid AAD token. Token expiration is the most common cause for a token to become invalid. By default, the connection token is valid for one hour. Be sure to use a valid token to connect to your database successfully. This issue may also occur if any of the registered claims in the identity(ID) token are invalid. See the documents below for more information.
<!--/issueDescription-->

## **Recommended Documents**

* [Obtaining Azure Active Director (AAD) Connection token](https://blogs.technet.microsoft.com/stefan_stranger/2018/06/06/connect-to-azure-sql-database-by-obtaining-a-token-from-azure-active-directory-aad/)
* [Understanding JWT identity Claims for AAD Connection Token](https://docs.microsoft.com/azure/architecture/multitenant-identity/claims)
