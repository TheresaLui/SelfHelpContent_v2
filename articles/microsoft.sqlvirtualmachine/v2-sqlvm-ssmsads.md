<properties
  pagetitle="Tools like SSMS, Azure Data Studio &#xD;"
  description="Tools-Management Studio, Azure Data Studio"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740105"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="446f196d-a2bf-4785-9cd0-83674088e421"
  ownershipid="AzureData_AzureSQLVM" />
# Tools like SSMS, Azure Data Studio 

Resolve issues with tools like SSMS and Azure Data Studio by using the following steps. 

## **Recommended Steps** 

 * **If you're having issues with SQL Server Management Studio or Azure Data Studio, make sure you're using [the latest build of SQL Server Management Studio](https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15) or [the latest build of Azure Data Studio](https://docs.microsoft.com/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15) to avoid any known issues.** We release updates for SSMS and ADS monthly.

- **Expanding database in SSMS/Azure Data Studio takes longer/times out** 

   This can happen if you have too many database objects. See if you can reduce or delete the unwanted objects. 

- **"Error: Lock request timed out"** when using SSMS 

  When displaying information such as tables by operating the GUI of SSMS, a query is issued internally. If the resource accessed by the query is [locked](https://docs.microsoft.com/sql/t-sql/statements/set-lock-timeout-transact-sql?view=sql-server-ver15), a lock timeout will occur. 

- **Can't download Tools like SSMS, Azure Data Studio, SSDT** 

  Make sure you have internet connectivity on the Azure VM. 

- **Intellisense isn't working on some databases when using SSMS** 

   See [common issues](https://docs.microsoft.com/sql/ssms/scripting/troubleshooting-intellisense?view=sql-server-ver15). 

- [Install the SQL Server PowerShell Module](https://docs.microsoft.com/sql/powershell/download-sql-server-ps-module?view=sql-server-ver15).

## **Recommended Documents** 

* [Download link for the latest build of SQL Server Management Studio](https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15) 
* [Download link for the latest build of Azure Data Studio](https://docs.microsoft.com/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15) 
* [Get diagnostic data after a SQL Server Management Studio (SSMS) crash](https://docs.microsoft.com/sql/ssms/troubleshoot/ssms-troubleshoot?view=sql-server-ver15) 
* [Tutorial: Connect and query SQL Server using Azure Data Studio](https://docs.microsoft.com/sql/azure-data-studio/quickstart-sql-server?view=sql-server-ver15)
