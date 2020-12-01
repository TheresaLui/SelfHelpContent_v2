<properties
  pagetitle="Change SQL Server Version or Edition on Azure VM"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740074"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="41b95f50-cbd9-45b4-b21f-93558bfec911"
  ownershipid="AzureData_AzureSQLVM" />
# Change SQL Server Version or Edition on Azure VM

Most users can change the SQL Server version or edition on Azure VMs by using the steps below.

## **Recommended Steps**

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


## **Recommended Documents**

* [SQL Server supported version and edition upgrades](https://docs.microsoft.com/sql/database-engine/install-windows/supported-version-and-edition-upgrades-version-15?view=sql-server-ver15)  
* [FAQs about licensing](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/frequently-asked-questions-faq#licensing?WT.mc_id=Portal-Microsoft_Azure_Support)  
* [Register with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider?WT.mc_id=Portal-Microsoft_Azure_Support)
* [Change SQL Server version](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version)
* [Change SQL Server edition](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition)    
* [Change license model](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal)