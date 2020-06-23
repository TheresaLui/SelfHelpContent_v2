<properties
	pageTitle="SQL image provisioning"
	description="SQL image provisioning"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740092"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="11c09f5c-18a1-40b6-ae41-176dac796d53"
	ownershipId="AzureData_AzureSQLVM"
/>

# SQL image provisioning

If you are planning to deploy a SQL inside a Virtual Machine, follow the [Provision SQL Server using Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-server-provision) guide.

## Common Issues
* **Cannot find the SQL Image on Azure Portal** 

    * We have a lot of images in the backend which does not show up on Azure Portal as we maintain the latest versions on the portal. Use the below script and deploy the VM from PowerShell if it is available:

```
Login-AzureRmAccount
$X = @()
$SQLVer = "SQL2016"
$locals = Get-AzureRmLocation
foreach($local in $locals)
{
$X += Get-AzureRmVMImageOffer -Publisher 'MicrosoftSQLServer' -Location $local.DisplayName | Get-AzureRmVMImageSku | Where {($_.Offer).Contains($SQLVer)} 
}
$X | Get-AzureRMVMImage | Out-GridView -Title "Images" -PassThru
```
  
* **Changing SQL Collation**: Currently you cannot change the collation for SQL Server if you are provisioning an image from the Azure Marketplace. You need to [rebuild the system databases to change the collation](https://docs.microsoft.com/sql/relational-databases/collations/set-or-change-the-server-collation?view=sql-server-ver15) 
* **Changing Default Drive for SQL installation**: If you deploy any SQL Server Marketplace image then it is not possible to change the installation directory during provisioning. By default we will install the binaries in C drive. There are two ways you can achieve to have SQL binaries/installation on a different drive: <br>

	* Uninstall the SQL with Shared Features and install it on a new location on the same VM which you have<br>
	* Create a windows only VM and copy the SQL Setup file from the VM you currently have or from Volume licensing and install it on the desired location you want to. Post installation make sure you change the licensing using [SQL Resource Provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb?tabs=azure-portal) so that it reflects the correct billing for your VM.

* **Generalize SQL VM**: You have two ways to generalize SQL Server on Azure VM:

	* Start with OS only VM and follow regular two-step [SQL Sysprep process](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-using-sysprep?view=sql-server-ver15), followed by [Windows Sysprep](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)
	* Use one of our SQL VM images and use [Windows Sysprep](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource). If you are following this, make sure you [add SQL login to the generalized VM and you delete the registry key mentioned here](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#images).

## **Recommended Documents**

* [Install SQL with sysprep](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-using-sysprep?view=sql-server-ver15)<br>
* [Create Managed Image of Generalized VM](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>
* [FAQ on SQL Images](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#images)<br>
* [Provisioning SQL VM with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-ps-sql-create)<br>
* [Deploy SQL using Azure quickstart templates](https://azure.microsoft.com/resources/templates/?term=sql)<br>
* [Provision SQL Server from Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-server-provision)
