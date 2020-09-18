<properties
	pageTitle="Failed database Export using SAS key"
	description="Failed database Export using SAS key"
	infoBubbleText="Found recent failed database export using SAS key. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authorAlias="vitomaz"
	ms.author="vitomaz"
	authors="vitomaz-msft"	
	displayOrder=""
	articleId="sql_ie_errorexportingdatabasefromportal"
	diagnosticScenario="SqlRca"
	selfHelpType="rca"
	supportTopicIds="32630420"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_ImportExport"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
At least one database on this server faced a failed export operation using a SharedAccessKey. We recently identified a regression in the import/export service that is generating incorrect SAS tokens to the storage accounts causing the following error:
Error encountered during the service operation. Blob ....bacpac is not writeable. The remote server returned an error: (403) Forbidden.
The engineering team has rolled out the fix, but it might take some time for the fix to get applied worldwide.
<!--/issueDescription-->
<br>

## **Recommended Steps**

Click this link to access the [Azure Portal](https://portal.azure.com/?feature.canmodifystamps=true&microsoft_azure_storage=stage1) and perform the export operation from that version. The portal shows an orange title bar if you open it via the above link, this is expected.

Other alternatives are:

- Use [sqlpackage.exe](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility)
- Use SSMS
- Use [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.sql/new-azurermsqldatabaseexport?view=azurermps-6.13.0)
