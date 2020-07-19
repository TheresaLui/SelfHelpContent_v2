<properties
	pageTitle="SQL Server Setup or patching"
	description="SQL Server Setup or patching"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740100"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="08d70dfd-4a85-4c6a-b47f-177c66a6f806"
	ownershipId="AzureData_AzureSQLVM"
/>



# SQL Server Setup or patching


## Common Issues

* **Can I install a second instance of SQL Server on the same VM? Can I change installed features of the default instance? Where can I find the installation Setup file?**

    Yes. The SQL Server installation media is located in a folder on the C drive. Run Setup.exe from that location to add new SQL Server instances or to change other installed features of SQL Server on the machine. Note that some features, such as Automated Backup, Automated Patching, and Azure Key Vault Integration, only operate against the default instance, or a named instance that was configured properly 

* **Can I remove SQL Server completely from a SQL Server VM?**

    Yes, but you will continue to be charged for your SQL Server VM as described in [Pricing guidance](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-pricing-guidance) for SQL Server Azure VMs. If you no longer need SQL Server, you can deploy a new virtual machine and migrate the data and applications to the new virtual machine. Then you can remove the SQL Server virtual machine.
	
* **Where can I get the setup media to change the edition or version of SQL Server?**


  Customers who have [software assurance](https://www.microsoft.com/licensing/licensing-programs/software-assurance-default?rtc=1&activetab=software-assurance-default-pivot%3aprimaryr3) can obtain their installation media from the [Volume Licensing Center](https://www.microsoft.com/Licensing/servicecenter/default.aspx). Customers that do not have software assurance can use the setup media from a Marketplace SQL Server VM image that has their desired edition.

* **How do I change to a different version/edition of the SQL Server in an Azure VM?**

  Customers can change their version/edition of SQL Server by using setup media that contains their desired version or edition of SQL Server. Once the edition has been changed, use the Azure portal to modify the edition property of the VM to accurately reflect billing for the VM. For more information, see [change edition](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-change-edition) of a SQL Server VM. There is no billing difference for different versions of SQL Server, so once the version of SQL Server has been changed, no further action is needed.
  
* **How are updates and service packs applied on a SQL Server VM?**

  Virtual machines give you control over the host machine, including when and how you apply updates. For the operating system, you can manually apply windows updates, or you can enable a scheduling service called [Automated Patching](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-automated-patching). Automated Patching installs any updates that are marked important, including SQL Server updates in that category. Other optional updates to SQL Server must be installed manually.
  
* **How can I get free extended security updates for my end of support SQL Server 2008 and SQL Server 2008 R2 instances?**

  You can get [free extended security updates](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-2008-eos-extend-support) by moving your SQL Server as-is to an Azure SQL virtual machine. For more information, see [end of support options](https://docs.microsoft.com/sql/sql-server/end-of-support/sql-server-end-of-life-overview?view=sql-server-ver15).


## **Recommended Steps**

Please make sure you upload the setup bootstrap folder if there are any issues/errors you encounter installing a Cumulative update, Security patch, Service pack or a new instance while raising a support case with Microsoft. The folder can be found at the location: _**%programfiles%\Microsoft SQL Server\130\Setup Bootstrap\Log**_ where 130 is the version of SQL 2016 installed on the machine.

## **Recommended Documents**

* [Setup and Patching FAQ](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#updating-and-patching)<br>
* [Change SQL Edition](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-change-edition)<br>
* [Automated Patching Feature](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-automated-patching)<br>
* [Information on installing updates](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-servicing-updates?view=sql-server-ver15)<br>
