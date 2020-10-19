<properties
  pagetitle="General Licensing Questions"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="amamun"
  selfhelptype="Generic"
  supporttopicids="32740081"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="deefbfc5-9904-4cad-ad74-d95e0ed297c3"
  ownershipid="AzureData_AzureSQLVM" />
# General Licensing Questions

Most users can resolve general questions about licensing by following the steps below.

## **Recommended Steps** 

**Why do I see SQL Virtual Machine Resource? Who created it? Do I get billed for this?**
SQL Virtual Machine Resource Provider (RP) is a free resource that gives you management capability of the SQL VM from the portal. SQL VM RP is created when you deploy a SQL VM image. Azure can also create this resource automatically on an existing VM if a SQL instance is detected. There is no cost associated with SQL VM RP.

**Why I am unable to change licensing model or manage SQL server from Azure portal?**
If you are unable to change licensing model or manage SQL server from Azure portal, make sure that [SQL VM Resource Provider (RP) is registered](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash).

**Why I am unable to register the SQL VM Resource Provider (RP)?**
If you are [unable to register the SQL VM Resource Provider (RP)](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash), check the prerequisites for SQL VM RP - 
  - SQL Server engine is installed as default instance or if there is no default instance there is only one named instance. SQL VM RP does not work if there is no default instance and there are multiple named instances. 
  - SQL instance is not evaluation edition.

**How do I estimate my cost for SQL Server on Azure VM? How do I reduce cost for SQL VM?**
Use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to configure and estimate the cost of SQL Server on Azure VM. For ways to reduce SQL VM cost, see [Reduce costs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/pricing-guidance#reduce-costs).    

**Why am I getting charged even though the SQL instance is stopped or the Azure VM is stopped?** 
To stop the billing, Azure VM must be in a deallocated state. You can deallocate Azure VM from the management portal or through PowerShell. Ensure that the VM is in the status Stopped (Deallocated) in the Azure Portal. If you shut down your SQL Server instance or your VM from the OS itself, it will not be deallocated, and charges will continue.   
 
**How do I change SQL VM license model to Azure Hybrid Benefit (BYOL), or pay-as-you-go, or Disaster Recovery?**
To make any of these changes, follow the instructions in [change license model](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal)  
  
**How do I get installation media or the product key?**
- To get SQL Server installation media, use an existing SQL Server VM or deploy a SQL Server VM from the Azure marketplace that has the desired edition and version of SQL Server. The setup media is located at C:\SQLServerFull of the SQL VM. 
- To get the SQL Server setup product key, launch `setup.exe` from C:\SQLServerFull on the SQL Azure VM that has the desired edition and version, copy the product key that appears in the install process, and then exit the installer 

**How do I upgrade or downgrade Edition or Version of a SQL VM?**
To upgrade or downgrade, follow the instructions in [change the SQL edition](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition) or [change the SQL version](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version).     

**How do I upgrade from the Evaluation edition?**
To upgrade from the Evaluation edition on the same VM: 
- Get the product key: Launch setup.exe located at C:\SQLServerFull from another SQL Azure VM that has the desired edition and version, copy the product key that appears in the install process, and then exit the installer. 
- Follow the instructions in [upgrade edition](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition) article.   

**What is SQL Developer edition? Is there a free SQL edition?**
[SQL Developer](https://www.microsoft.com/sql-server/sql-server-downloads)is a full-featured free edition, licensed for use as a development and test database in a non-production environment. The limited-feature [SQL Express edition](https://www.microsoft.com/sql-server/sql-server-downloads) is also free and can be used in a production environment. Note that only SQL licensing for these editions is free. You will be billed for additional resources such as VM, storage, and so on. 
You can deploy SQL images with free editions. If you install these editions on a Windows-only VM, we strongly recommend that you [register with SQL VM RP](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash).  

**How can I determine the license type of my SqlVirtualMachine resources?**
Run the following Powershell command:   
`(Get-AzureRmResource -ResourceName <vm_name> -ResourceGroupName <resource_group> -ResourceType 'Microsoft.SqlVirtualMachine/SqlVirtualMachines').Properties | Format-List;` 
     
## **Recommended Documents** 
* [Frequently Asked Questions (FAQ)](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq?WT.mc_id=Portal-Microsoft_Azure_Support) for SQL Server on Azure VM 
* [Pricing guidelines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-pricing-guidance?WT.mc_id=Portal-Microsoft_Azure_Support) for SQL Server on Azure VM