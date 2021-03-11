<properties
  pagetitle="Change Licensing Model"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740073"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="c0b11a20-dda3-463c-9ce9-a22c1a8cbdd8"
  ownershipid="AzureData_AzureSQLVM" />
# Change Licensing Model

Most users who want to change the licensing model of SQL Server on Azure VM can resolve issues by using the following information.

## **Recommended Steps**

- To change licensing model of SQL Server on Azure VM, follow the instructions at [Change license model](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal&WT.mc_id=Portal-Microsoft_Azure_Support). You'll be able to change the licensing to or from pay-as-you-go, Azure Hybrid Benefit (Bring your own license: BYOL), or disaster recovery (DR). **For Azure China Government Cloud(MoonCake), PAYG/AHB conversion is currently not allowed.**

- To change SQL Server **version or edition** on Azure VM:

  - To upgrade or downgrade the SQL **version**, see [in-place Change of SQL Server Version on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version). Example: Change the version to or from SQL Server 2008, 2008R2, 2012, 2016, 2017, 2019, and so on. 
  - To upgrade or downgrade the SQL **edition**, see [in-place change of SQL Server edition on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition). Example: Change the edition to or from SQL edition Standard, Enterprise, Express, Developer, Web.

- To get SQL Server **installation media**, go to C:\SQLServerFull from an Azure Marketplace SQL Server VM image with the desired edition and version

- To get a SQL Server setup **product key**, launch `setup.exe` from C:\SQLServerFull on the Azure VM that has the desired edition and version, copy the product key that appears in the install process, and exit the installer

- To **remove SQL Server instance and the associated SQL billing** from a pay-as-you-go SQL VM, or if you are **getting charged for SQL instance after uninstalling it**: 
  - If necessary, after backing up your data, uninstall SQL Server completely, including the SQL IaaS extension   
  - Install the free [SQL Express](https://www.microsoft.com/sql-server/sql-server-downloads) edition 
  - Install SQL IaaS Agent Extension in [lightweight mode](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash)
 
## **Recommended Documents**

* [Licensing FAQ](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/frequently-asked-questions-faq#licensing?WT.mc_id=Portal-Microsoft_Azure_Support) for SQL Server on Azure Virtual Machine 
* [Change the licensing model for a SQL VM in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal)
* [In-place change of SQL Server version on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version)
* [In-place change of SQL Server edition on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition)
* [Licensing FAQ for SQL Server on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/frequently-asked-questions-faq#licensing)
* [Register SQL Server VM in Azure with SQL IaaS Agent Extension](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider)
* [Software Assurance](https://www.microsoft.com/licensing/licensing-programs/software-assurance-default?activetab=software-assurance-default-pivot%3aprimaryr3) overview