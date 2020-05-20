<properties
	pageTitle="Change SQL Server Version or Edition on Azure VM"
	description="Change SQL Server Version or Edition on Azure VM"
	service="microsoft.compute"
	resource="virtualmachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	articleId="41b95f50-cbd9-45b4-b21f-93558bfec911"
	selfHelpType="generic"
	supportTopicIds="32740074"
	resourceTags="WindowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="AzureData_AzureSQLVM"
/>

# Change SQL Server Version or Edition on Azure VM

## **Recommended Steps**

Please follow the below steps to change SQL Server Version or Edition on Azure VM:

1. Backup all systems and user databases
2. Get the installation media. If you have software assurance, you can obtain their installation media from the Volume Licensing Center. If you do not have software assurance, you can use the setup media from a Marketplace SQL Server VM image that has their desired edition.
3. Upgrade [the SQL Version](https://docs.microsoft.com/sql/database-engine/install-windows/upgrade-sql-server?view=sql-server-ver15) or [the SQL Edition](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-change-edition). Please note that downgrade of edition or version requires complete un-install and re-install of the SQL instance. 
4. Ensure that you have [registered the SQL Azure VM with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider?tabs=azure-cli%2Cbash)
5. For edition changes, [change the edition in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-change-edition#change-edition-in-portal).

As there is no billing difference for different versions of SQL Server, once the version of SQL Server has been changed, no further action is needed.

## **Recommended Documents**

* [Change the license model for a SQL Server virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal)
* [Register SQL Server virtual machine in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider)
* [Virtual Machines Licensing FAQ](https://azure.microsoft.com/pricing/licensing-faq/)
