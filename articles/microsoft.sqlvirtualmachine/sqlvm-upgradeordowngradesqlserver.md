<properties
	pageTitle="sql administration/upgrade or downgrade SQL"
	description="sql administration/upgrade or downgrade SQL"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="yareyes"
	ms.author="yareyes"
	displayOrder=""
	articleId="d2598f27-28fd-42ac-9375-280df1d0933f"
	selfHelpType="generic"
	supportTopicIds="32633525"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax"
	ownershipId="AzureData_AzureSQLVM"
/>

# sql administration/upgrade or downgrade SQL

* **How do I change to a different edition of the SQL Server in an Azure VM?**

	1. Customers can change their edition of SQL Server by using setup media that contains their desired edition of SQL Server as listed in the self-help below. See [Change edition of a SQL Server VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-change-edition) for steps to upgrade or downgrade edition. While downgrading edition you must ensure you are not using any feature that is available only on the higher edition.
	2. Once the edition has been changed, remember to use the Azure portal to modify the edition property of the SQL VM to accurately reflect billing for the VM

* **How do I upgrade the version of SQL server in an Azure VM?**

	1. Customers can upgrade their version of SQL Server by using setup media that contains their desired version of SQL Server as listed in the self-help below. See [Upgrade SQL Server Using the Installation Wizard](https://docs.microsoft.com/sql/database-engine/install-windows/upgrade-sql-server-using-the-installation-wizard-setup) for steps to upgrade the version.
	2. Note that if the upgraded edition is different from the previous setting, you will need to [change edition of the SQL Server VM in Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-change-edition) to accurately billing for the SQL VM
	
* **Can I remove SQL Server completely from a SQL VM?**

	You can uninstall SQL Server on Azure VM by using the installation media located on the VM OS drive. But this will not remove any SQL Server license related charges associated with the VM. If you do not need the SQL VM you should stop/deallocate the VM to stop any further charges.
	
* **How do I obtain the installation media for SQL Server to change edition or version in my Azure VM?**

	Customers who have [Software Assurance](https://www.microsoft.com/Licensing/licensing-programs/software-assurance-overview) and have access to [Volume Licensing Center](https://www.microsoft.com/Licensing/servicecenter/default.aspx) can obtain the installation media from the Center.

	Alternately, you can use the setup media from a marketplace SQL Server VM image that has the desired version and edition. The following steps explain how to do this: 
	1. Either use an existing SQL Server VM, or deploy a SQL Server VM from the Azure marketplace that has the desired edition of SQL Server
	2. RDP into this new SQL Server VM and navigate to where the SQL Server setup media is: ***C:\SQLServerFull***
	3. Copy over the directory to the intended VM and launch setup.exe
	4. If you created a new VM to obtain the media, remember to delete it to avoid the billing costs

	Another alternative is to download the SQL evaluation edition on your VM and use the product key form a marketplace SQL Server VM image that has the desired version and edition. To get the product key, you can launch setup.exe from ***C:\SQLServerFull*** on the Azure VM that has desired edition and version, copy the product key that appears in the install process and exit the installer. 

##  **Recommended Documents**

* [Frequently asked questions for SQL Server running on Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq)<br>

* [How to change licensing model for a SQL Server virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal)<br>

* [Register SQL Server virtual machine in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider)
