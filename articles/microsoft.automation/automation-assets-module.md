<properties
    pageTitle="Azure Automation - I need help updating or importing a module"
    description="Azure Automation - Updating and importing modules"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32628005,32628012"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="7520716a-1463-4666-b9d2-60f15be30964"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Updating or Importing Modules

An Automation Account, when created, only has a small subset of Azure modules included. 

This article contains information about updating the modules contained in your Automation Account.

## **Recommended Steps**

Before continuing in this document, please review the [notes found in the Update Modules document](https://docs.microsoft.com/azure/automation/automation-update-azure-modules#update-azure-modules-in-the-azure-portal). It is recommended to have a test Automation Account to ensure updating modules do not impact your existing scripts. 

### **A module I imported does not work in Azure Automation sandbox environments**

* Some modules may have dependencies on binaries which are not supported in Azure Automation sandboxes. Scripts which require these modules should be run via [a hybrid worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). 

### **I am using Az modules in Azure Automation**

* While Az modules are supported in Azure Automation, there are several important considerations. Review the [Az Module Support documentation](https://docs.microsoft.com/azure/automation/automation-update-azure-modules) for potential pitfalls, including using AzureRM modules in the same account as Az modules. 

### **Module import stuck, "importing newer version" stuck**

* If module imports are stuck, unsuccessful, or otherwise in a bad state, you can use PowerShell to remove the module and try again:

`Get-AzureRmAutomationModule -ResourceGroupName RGoftheAAAcount -AutomationAccountName YourAutomationAccount| Where-Object { $_.ProvisioningState -eq "Creating"} | Remove-AzureRmAutomationModule`

### **"The module is imported but not loaded"**

* Add an explicit ["Import-Module" statement](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/import-module?view=powershell-5.1) to the beginning of your runbook

## **Recommended Documents**

* [Common errors when importing modules](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#common-errors-when-importing-modules)<br>
* [Integration modules in Azure Automation](https://docs.microsoft.com/azure/automation/automation-integration-modules)<br>
* [Runbook and module galleries for Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-gallery)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
