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
	cloudEnvironments="public"
/>

# sql administration/upgrade or downgrade SQL

* **How do I change to a different version/edition of the SQL Server in an Azure VM?**

	Customers can change their version/edition of SQL Server by using setup media that contains their desired version or edition of SQL Server. Once the edition has been changed, use the Azure portal to modify the edition property of the VM to accurately reflect billing for the VM. For more information, see [change edition of a SQL Server VM.](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-change-edition)

* **Can I remove SQL Server completely from a SQL VM?**

	You can uninstall SQL Server on Azure VM by using the installation media located on the VM OS drive. But this will not remove any SQL Server license related charges associated with the VM. If you do not need the SQL VM you should stop/deallocate the VM to stop any further charges occur.

##  **Recommended Documents**

* [Frequently asked questions for SQL Server running on Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq)<br>

* [How to change licensing model for a SQL Server virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal)<br>

* [Register SQL Server virtual machine in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider)
