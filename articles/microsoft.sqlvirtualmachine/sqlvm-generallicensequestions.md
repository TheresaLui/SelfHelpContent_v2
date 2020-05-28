<properties
	pageTitle="licensing/general questions"
	description="licensing/general questions"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="yareyes"
	ms.author="yareyes"
	displayOrder=""
	articleId="13c5a3ba-a77b-448d-b8c7-fac44a9000a3"
	selfHelpType="generic"
	supportTopicIds="32633507"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="AzureData_AzureSQLVM"
/>

# licensing/general questions

* [What is End of Support for SQL Server and Windows Server 2008 and 2008 R2?](https://www.microsoft.com/cloud-platform/extended-security-updates)


* **How can I install my licensed copy of SQL Server on an Azure VM?**

	There are two ways to do this. You can provision one of the [virtual machine images that supports licenses](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-overview#BYOL), which is also known as bring-your-own-license (BYOL). Another option is to copy the SQL Server installation media to a Windows Server VM, and then install SQL Server on the VM. We recommend using one of the BYOL gallery images. To use BYOL or your own SQL Server media on an Azure VM, you must have [License Mobility through Software Assurance](https://azure.microsoft.com/pricing/license-mobility/) on Azure.

* **Do I have to pay to license SQL Server on an Azure VM if it is only being used for standby/failover?**

	If you have Software Assurance and use License Mobility as described in [Virtual Machine Licensing FAQ,](https://azure.microsoft.com/pricing/licensing-faq/) then you do not have to pay to license one SQL Server participating as a passive secondary replica in an HA deployment. Otherwise, you need to pay to license it.

* **Can I change a VM to use my own SQL Server license if it was created from one of the pay-as-you-go gallery images?**

	Yes. You can move easily move between the two licensing models, review [How to change licensing model for a SQL Server virtual machine in Azure.](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal)

* **Should I use BYOL images or SQL VM RP to create new SQL VM?**

	Bring-your-own-license (BYOL) images are only available for EA customers. Other customers who have Software Assurance should use the SQL VM resource provider to create a SQL VM with [Azure Hybrid Benefit (AHB).](https://azure.microsoft.com/pricing/licensing-faq/)

* **Will switching licensing models require any downtime for SQL Server?**

	No. Changing the licensing model does not require any downtime for SQL Server as the change is effective immediately and does not require a restart of the VM.
	To change the licensing model, the VM must be registered with SQL VM resource provider. Please review [Register SQL Server virtual machine in Azure with the SQL VM resource provider.](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider) to find out different modes of registering with SQL VM resource provider.

* **Will registering my VM with the new SQL VM resource provider bring additional costs?**

    No. The SQL VM resource provider just enables additional manageability for SQL Server on Azure VM with no additional charges.

* **Is the SQL VM resource provider available for all customers?**

	Yes. All customers are able to register with the new SQL VM resource provider. However, only customers with Software Assurance Benefit can activate the Azure Hybrid Benefit (AHB) (or BYOL) on a SQL Server VM.

* **Is it possible to register self-deployed SQL Server VMs with the SQL VM resource provider?**

	Yes. If you deployed SQL Server from your own media and installed the SQL IaaS extension you can register your SQL Server VM with the resource provider to get the manageability benefits provided by the SQL IaaS extension.

* **Where can I find the license key to use for installing SSRS or SSAS 2017+ in an Azure VM?**

	If you already have a SQL Server VM with Standard or Enterprise edition created from Azure Marketplace, you can launch setup.exe from ***C:\SQLServerFull***, copy the product key that appears in the install process and exit the installer. You can then apply the key during SSRS or SSAS installation. 

* **How can I determine the license type of my SqlVirtualMachine resources?**

	You can use the following Powershell command:  
	`(Get-AzureRmResource -ResourceName <vm_name> -ResourceGroupName <resource_group> -ResourceType 'Microsoft.SqlVirtualMachine/SqlVirtualMachines').Properties | Format-List;`


##  **Recommended Documents**

* [Frequently asked questions for SQL Server running on Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq)
* [Pricing guidance for Azure SQL Server VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-pricing-guidance)
