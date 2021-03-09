<properties
  pagetitle="SQL Server exceptions, crashes, dumps"
  description="SQL Server exceptions, crashes, dumps"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740096"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="761cce48-2167-4785-a8b7-bd1c70d0e2ab"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Server exceptions, crashes, dumps


4 out of 5 customers are able to resolve their issues with SQL Server exceptions, crashes, dumps using the following steps.

## **Recommended Steps**

**To avoid such crashes and dumps,Please make sure**
- SQL Server and its components are [up to date to the latest build](https://support.microsoft.com/help/321185/how-to-determine-the-version-edition-and-update-level-of-sql-server-an)
- All user and system databases are [corruption free](https://docs.microsoft.com/sql/relational-databases/maintenance-plans/check-database-integrity-task-maintenance-plan?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)
- [Do not use third party detours](https://docs.microsoft.com/troubleshoot/sql/general/issue-detours-similar-techniques) in order to avoid unexpected behavior
- Move third-party objects, [COM objects](https://docs.microsoft.com/troubleshoot/sql/admin/run-dll-based-com-object) or [Linked 
servers](https://docs.microsoft.com/sql/relational-databases/linked-servers/create-linked-servers-sql-server-database-engine?view=sql-server-ver15#to-view-the-provider-options) outside the SQL Server processes 
- Ensure that there is no resource crunch. To check VM or disk level IO capping, you can [check this article](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows?WT.mc_id=Portal-Microsoft_Azure_Support#storage-io-utilization-metrics). 
- Ensure that SQL Server is [optimized](https://docs.microsoft.com/archive/msdn-magazine/2008/january/sql-server-uncover-hidden-data-to-optimize-application-performance?WT.mc_id=Portal-Microsoft_Azure_Support):- 
  - You follow the [Performance Guidelines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support)
  - Consider adding [missing indexes](https://gallery.technet.microsoft.com/Find-statements-for-13e8c2f4) 
  - Consider [updating statistics](https://docs.microsoft.com/sql/relational-databases/maintenance-plans/update-statistics-task-maintenance-plan?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support), if possible with Full Scan, for the tables of database(s) that are frequently modified
- Azure VM size and disk capacity meet or exceed the load. 
- Windows operating system and its components like .NET framework are up to date to the latest build
- If above items does not solve your issue and you decide to open a service request, please **share the SQL dumps (*.mdmp files) and logs** with Microsoft.

## **Recommended Documents**

- [Where to find information about the latest SQL Server builds](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds)
- Detours or similar techniques [may cause unexpected behaviors](https://docs.microsoft.com/troubleshoot/sql/general/issue-detours-similar-techniques)
- How to use the [Sqldumper.exe utility to generate a dump file in SQL Server](https://support.microsoft.com/help/917825/use-the-sqldumper-exe-utility-to-generate-a-dump-file-in-sql-server)
- [Database Engine Error List](https://docs.microsoft.com/sql/relational-databases/errors-events/database-engine-events-and-errors?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)