<properties
	pageTitle="how to/multiple instances on azure vm"
	description="how to/multiple instances on azure vm"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="yareyes"
	ms.author="yareyes"
	displayOrder=""
	articleId="9b8c3bf9-1135-49af-aa3d-93ace14d199e"
	selfHelpType="generic"
	supportTopicIds="32633511"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax"
	ownershipId="AzureData_AzureSQLVM"
/>

# how to/multiple instances on azure vm

* **Can I install a second instance of SQL Server on the same VM? Can I change installed features of the default instance?**

    Yes. The SQL Server installation media is located in a folder on the C drive. Run Setup.exe from that location to add new SQL Server instances or to change other installed features of SQL Server on the machine. Note that some features, such as Automated Backup, Automated Patching, and Azure Key Vault Integration, only support one SQL instance installed.

* **Can I uninstall the default instance of SQL Server?**

    Yes, but there are some considerations. If you uninstall the default instance, [SQL Server IaaS Agent Extension](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension) continues to look for the default instance and may generate event log errors. These errors are from the following two sources: Microsoft SQL Server Credential Management and Microsoft SQL Server IaaS Agent. One of the errors might be similar to the following:

    A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible.

    If you do decide to uninstall the default instance, also uninstall the SQL Server IaaS Agent Extension as well. After installing the new SQL instance, please re-install the SQL Server IaaS Agent Extension.

* **Can I remove SQL Server completely from a SQL VM?**

    Yes, but you will continue to be charged for your SQL VM as described in [Pricing guidance for SQL Server Azure VMs.](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-pricing-guidance) If you no longer need SQL Server, you can deploy a new virtual machine and migrate the data and applications to the new virtual machine. Then you can remove the SQL Server virtual machine.


##  **Recommended Documents**

* [Frequently asked questions for SQL Server running on Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq)
