<properties
	pageTitle="Errors when creating or deleting a DMS"
	description="Top errors and troubleshooting info for DMS service creation and deletion"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="service-create-or-delete-failure"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32673608"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting errors while creating or deleting Database Migration Service instance

## **Recommended Steps**

### Create Service Errors

**Error:** 

* *"SubnetWithExternalResourcesCannotBeUsedByOtherResources"* 
* *"xxx/NIC-xxxxxxxxxxxx/ipConfigurations/ipconfig cannot be used because it contains external resources."*
* *"You need to ***delete these external resources*** before deploying into this subnet."*

### **Recommened Steps**

* The VNET selected to create DMS instance in contained external resources like application gateway, Azure SQL DB Managed Instance, or hosting environments. DMS can be created in the same VNET but it needs to be created in a separate Subnet. 

**Error:** 

* *"VM has reported a failure when processing extension **'CustomScriptExtension'**. Error message: "Finished executing command."*

### **Recommended Steps** 

* This error most commonly occurs when the VNET selected to create a DMS instance is blocking connectivity to the metrics and health monitoring end point https://prod.warmpath.msftcloudes.com and/or blocking the following communication ports: 443, 53, 9354, 
445, 12000

### **Recommended Documents**

* [Common Network Configuration Issues](https://docs.microsoft.com/azure/api-management/api-management-using-with-vnet#-common-network-configuration-issues)<br>
* [Overview of prerequisites for using the Azure Database Migration Service](https://docs.microsoft.com/azure/dms/pre-reqs)

**Error:** 

* *"ServiceProvisioningDisabledException"*
* *"The service could not be provisioned. Please contact Microsoft with error code 'xxxx-<region_name>'"*

### **Recommended Steps** 

* DMS service may not be available in the region you are trying to create an instance. Check this website for 
availability by region: https://azure.microsoft.com/global-infrastructure/services/?products=database-migration&regions=all

**Error:** 

* *"ResourceNotPermittedOnDelegatedSubnet"*<br>

### **Recommended Steps** 

* The subnet used is a Delegated Subnet and dms service cannot be created in one

### **Recommended Documents**

* [Add, change, or delete a virtual network subnet](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet)

## Delete Service Errors

**Error:** 

* *"Service failed to Stop. Error: {'error':{'code':'InvalidRequest','message':'One or more activities are currently running. To
 stop the service, please wait until the activities have completed or stop those activities manually and try again.'}}"*

### **Recommended Steps** 

When this error is reported, it is possible that there are activities or tasks off projects that may not be visible on the Azure portal. This removes the ability to clean up DMS instance by deleting the service instance which requires the deletion of all tasks in all projects across service using the UI.

In such situation, use the Azure Resource Manager PowerShell module for Data Migration with below steps to clean up:

1.  Install-Module -Name AzureRM.DataMigration
2.  Login-AzureRmAccount
3.  Select-AzureRmSubscription -SubscriptionName "<subscription_Name>"
4.  Remove-AzureRmDataMigrationProject -Name <project_Name> -ResourceGroupName <rg_Name> -ServiceName <service_Name> -DeleteRunningTask 

Once this is done, try deleting the service again.

### **Recommended Documents**

* [Data Migration specific PowerShell cmdlets](https://docs.microsoft.com/powershell/module/azurerm.datamigration/?view=azurermps-6.13.0#data_migration)
