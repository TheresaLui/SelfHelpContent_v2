<properties
	pageTitle="Change Licensing Model- Pay As You Go or Bring Your Own"
	description="Change Licensing Model- Pay As You Go or Bring Your Own"
	service="microsoft.compute"
	resource="virtualmachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	articleId="c0b11a20-dda3-463c-9ce9-a22c1a8cbdd8"
	selfHelpType="generic"
	supportTopicIds="32740073"
	resourceTags="WindowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	ownershipId="AzureData_AzureSQLVM"
/>

# Change Licensing Model- Pay As You Go or Bring Your Own

## **Recommended Steps**

To change **licensing model of SQL Server on Azure VM** from Pay As you Go to Bring your own license or Azure Hybrid benefit please follow instructions to [Change the license model for a SQL virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal)

To change SQL Server Version or Edition on Azure VM:

- To upgrade or downgrade SQL **Version** (example - change version to and from SQL Server 2008/2008R2/2012/2016/2017/2019 etc.) please follow article [In-place Change of SQL Server Version on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version)
- To upgrade or downgrade SQL **Edition** (example - change edition to and from SQL edition Standard/Enterprise/Express/Developer/Web ) please follow article [In-place change of SQL Server edition on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition)

To get SQL Server **installation media**, please follow these steps:

* If you have [Software Assurance](https://www.microsoft.com/Licensing/licensing-programs/software-assurance-overview?rtc=1),
 you can obtain their installation media from the [Volume Licensing Center](https://www.microsoft.com/Licensing/servicecenter/default.aspx)
* If you have do not have Software Assurance, you can use the setup media from a marketplace SQL Server VM image that has the desired version and edition. The following steps explain how to do this:

	- Either use an existing SQL Server VM, or deploy a SQL Server VM from the Azure marketplace that has the desired edition and version of SQL Server
	- RDP into this new SQL Server VM and navigate to where the SQL Server setup media is: C:\SQLServerFull
	- Copy over the directory to the intended VM and launch setup.exe
	- If you created a new VM to obtain the media, remember to delete it to avoid the billing costs
	
Another alternative is to download the SQL evaluation edition on your VM and use the product key from a marketplace SQL Server VM image that has the desired version and edition. To get the product key, you can launch setup.exe from C:\SQLServerFull on the Azure VM that has desired edition and version, copy the product key that appears in the install process and exit the installer.

To get SQL Server setup **product key**, you can launch setup.exe from C:\SQLServerFull on the Azure VM that has desired edition and version, copy the product key that appears in the install process and exit the installer.

## **Recommended Documents**

* [Change the license model for a SQL virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal)
* [In-place Change of SQL Server Version on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version)[In-place change of SQL Server edition on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition)
* [In-place change of SQL Server edition on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition)
* [Licensing Frequently asked questions for SQL Server on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/frequently-asked-questions-faq#licensing)
* [Register SQL Server virtual machine in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider)
