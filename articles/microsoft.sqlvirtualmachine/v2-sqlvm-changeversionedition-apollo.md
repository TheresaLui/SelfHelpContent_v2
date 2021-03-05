<properties
	pagetitle="Change SQL Server Version or Edition on Azure VM"
	description="Change SQL Server Version or Edition on Azure VM"
	ms.author="amamun,ujpat"
	articleId="2078907c-e64a-437f-b6d2-b300f1fd3682" 
	selfHelpType="Apollo" 
  supportTopicIds="f97f5d64-542b-37ed-b0ce-b16b74faed62" 
  productPesIds="14745,16342" 
	cloudEnvironments="public,fairfax,usnat,ussec,blackforest,mooncake" 
	ownershipId="AzureData_AzureSQLVM" 
/>

# Change SQL Server Version or Edition on Azure VM

## Resolve issues with Change SQL Server Version or Edition on Azure VM

:::Section Metrics and Diagnostics:::  

### Change SQL Server Version or Edition on Azure VM

<insight>
    <symptomId>SqlVmHADRPortalInsight</symptomId>
    <executionText>We are running analysis check to find the steps to resolve</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
    <noResultText>No issues found</noResultText>
    <additionalInputsReq>true</additionalInputsReq>
    <maxInsightCount>1</maxInsightCount>
</insight>

### Recommended Steps 

Most users are able to resolve their issues using the following steps.

- To change SQL Server **version or edition** on Azure VMs:
  - To [upgrade or downgrade the SQL Server version](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version?WT.mc_id=Portal-Microsoft_Azure_Support), see [in-place change of SQL Server version on Azure VMs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version). Example: If you want to change the version of SQL Server to or from 2008, 2008R2, 2012, 2016, 2017, 2019, and so on.
  - To [upgrade or downgrade the SQL Server edition](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition?WT.mc_id=Portal-Microsoft_Azure_Support), see [in-place change of SQL Server edition on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition). Example: if you want to change edition to or from SQL edition Standard, Enterprise, Express, Developer, or Web. 

- To **change the licensing model** of SQL Server on Azure VM from or to pay-as-you-go, Azure Hybrid Benefit (bring your own license), or disaster recovery, see [change the licensing model](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal) 
- To get SQL Server **installation media**, use an existing SQL Server VM or deploy a SQL Server VM from the Azure marketplace that has the desired edition and version of SQL Server. The setup media is located at C:\SQLServerFull of the SQL VM. 
- To get the SQL Server **setup product key**, launch `setup.exe` from C:\SQLServerFull on the Azure VM that has the desired edition and version, copy the product key that appears in the install process, and exit the installer 


- If you are **unable to change licensing model or manage SQL server from Azure portal**, make sure that [SQL IAAS Extension is registered](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash).
- If you are **[unable to register the SQL IAAS Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash)**, check the prerequisites for SQL IAAS Extension - 
  - SQL Server engine is installed as default instance or if there is no default instance there is only one named instance. SQL VM RP does not work if there is no default instance and there are multiple named instances. 
  - SQL instance is not evaluation edition.




### Recommended Documents 
- [Monitor and troubleshoot Always On Availability Groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support) Availability Groups
- [Monitor performance](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/monitor-performance-for-always-on-availability-groups?view=sql-server-ver15) for Always On availability groups
- Troubleshoot: Availability Group exceeded [RPO](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-availability-group-exceeded-rpo?view=sql-server-ver15) or [RTO](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-availability-group-exceeded-rto?view=sql-server-ver15)
- [Changes from the primary replica are not reflected](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-primary-changes-not-reflected-on-secondary?view=sql-server-ver15) on secondary
- [Useful tools for Availability Group troubleshooting](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/useful-tools-for-troubleshooting?view=sql-server-ver15)
- [Recommendations for index maintenance](https://techcommunity.microsoft.com/t5/sql-server-support/recommendations-for-index-maintenance-with-alwayson-availability/ba-p/318518) with Availability Groups
