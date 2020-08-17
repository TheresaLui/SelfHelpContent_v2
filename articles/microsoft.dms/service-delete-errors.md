<properties
	pageTitle="Errors when deleting a DMS"
	description="Top errors and troubleshooting info for DMS service deletion"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="service-delete-errors"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743220"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting errors while deleting Database Migration Service instance

## Delete Service Errors

**Error:** 

* *"Service failed to Stop. Error: {'error':{'code':'InvalidRequest','message':'One or more activities are currently running. To
 stop the service, please wait until the activities have completed or stop those activities manually and try again.'}}"*

## **Recommended Steps** 

When this error is reported, it is possible that there are activities or tasks off projects that may not be visible on the Azure portal. This removes the ability to clean up DMS instance by deleting the service instance which requires the deletion of all tasks in all projects across service using the UI.

In such situation, use the Azure Resource Manager PowerShell module for Data Migration with below steps to clean up:

1.  Install-Module -Name AzureRM.DataMigration
2.  Login-AzureRmAccount
3.  Select-AzureRmSubscription -SubscriptionName "<subscription_Name>"
4.  Remove-AzureRmDataMigrationProject -Name <project_Name> -ResourceGroupName <rg_Name> -ServiceName <service_Name> -DeleteRunningTask 

Once this is done, try deleting the service again.

## **Recommended Documents**

* [Data Migration specific PowerShell cmdlets](https://docs.microsoft.com/powershell/module/azurerm.datamigration/?view=azurermps-6.13.0#data_migration)
