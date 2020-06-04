<properties
pageTitle="AAD Connect database(s) are running out of space"
	description="AAD Connect database(s) are running out of space"
	infoBubbleText="AAD Connect database(s) are running out of space"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_SqlDatabaseSizeCloseTo10GB"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# AAD Connect database(s) are running out of space
<!--issueDescription-->
There are some AADConnect server(s) whose databases are running low in storage space. Details: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
Azure AD Connect requires a SQL Server database to store identity data. You can either use the default SQL Server 2012 Express LocalDB installed with Azure AD Connect or full SQL. SQL Server Express imposes a 10-GB size limit. When using LocalDB and this limit is reached, Azure AD Connect Synchronization Service can no longer start or synchronize properly. Please look at the provided links to address this problem:

- [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-recover-from-localdb-10gb-limit)
- [Move Azure AD Connect database from SQL Server Express to SQL Server](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-move-db)
