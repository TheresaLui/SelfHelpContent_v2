<properties
	pageTitle="Check for sync agent cmdlet errors"
	description="Check for sync agent cmdlet errors"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32675708"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="59aa3418-5ad6-473c-b3c0-d669f8f9bf9f"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# How to check for sync agent cmdlet errors

**Problem:** While running the cmdlet, you may see the below error

~~~powershell

WARNING: Request failed with returned http error code : NotFound(404).

Reset-AzureRmStorageSyncServerCertificate : The resource was not found.

At line:1 char:1

+Reset-AzureRmStorageSyncServerCertificate -SubscriptionId 6c207442-3f ...

~~~

**Solution:** Install the required latest .Net framework, this error should go away. After installing the framework, you may see the below error

~~~powershell

WARNING: Both Az and AzureRM modules were detected on this machine. Az and AzureRM modules cannot be imported in the same session or used in the same script or runbook. If you are running PowerShell in an environment you control you can use the 'Uninstall-AzureRm' cmdlet to remove all AzureRm modules from your machine. If you are running in Azure Automation, take care that none of your runbooks import both Az and AzureRM modules. More information can be found here: https://aka.ms/azps-migration-guide

~~~

1. If you get the above error, proceed with uninstalling AzureRM by running the command "Uninstall-AzureRM".
2. You can't have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.
3. If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.
4. To do this, install PowerShell Core 6.x or later and then follow these instructions in a PowerShell Core terminal.

## **Recommended Documents**

1. [(Source Document)](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-2.8.0#install-the-azure-powershell-module-1)
