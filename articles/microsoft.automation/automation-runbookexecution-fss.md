<properties
    pageTitle="Troubleshoot Runbook Execution in Azure Automation"
    description="Troubleshoot Runbook Execution in Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder="201"
    selfHelpType="generic"
    supportTopicIds="32599908"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec, Mooncake"
    articleId="d6370ffa-48c7-48a5-9c4d-0dfd966ce672"
	ownershipId="Compute_Automation"
/>

# Troubleshoot Runbook Execution in Azure Automation

Here are some common issues with executing runbooks in Azure Automation and how to address them. Please note that Support will not write a new script for you based on your needs, but we will work with you to ensure your existing script executes correctly inside of Azure Automation. 

## **Recommended Steps**

Specific problems and their solutions are listed below, but we highly recommend you try these two troubleshooting steps first:

* Try running the [runbook locally](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#runbook-fails) before running it in Azure Automation. This can clarify if the issue is a bug in the runbook versus an issue with Azure Automation.
* Investigate runbook [error streams](https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#runbook-output) for specific messages and compare them to the errors below
* [Update the Azure PowerShell](https://docs.microsoft.com/azure/automation/automation-update-azure-modules) modules in your Automation Account to the latest version

### Runbook is suspended or unexpectedly failed

There are several reasons why a runbook may be suspended or failed:

* [Job Statuses](https://docs.microsoft.com/azure/automation/automation-runbook-execution#job-statuses) defines runbook statuses and some possible causes
* [Add additional output](https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#message-streams) to the runbook to identify what happens before the runbook is suspended
* [Handle any exceptions](https://docs.microsoft.com/azure/automation/automation-runbook-execution#handling-exceptions) that are thrown by your job
  * You may want to retry when certain exceptions, such as WebSocket exceptions, occur in order to prevent transient network failures from causing your runbook to fail
* If you are having issues with a specific cmdlet, you may find more relevant information with the service you are trying to use through the cmdlet. For example, New-AzAnalysisServicesServer issues might end up with the Analysis Services team. 

### Job was tried three times but it failed 

* Check the [Automation Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits), and consider moving to a [Hybrid Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker) if the limitation applies to Azure sandboxes only

### Runbook fails with "The subscription cannot be found" error

* This issue can occur when the runbook isn't using a RunAs account to access Azure resources. To resolve, follow the steps in [Scenario: Unable to find the Azure subscription](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#unable-to-find-subscription).

### "Your azure credentials have not been set up or have expired, please run connect-azureRmAccount to set up your azure credentials"

* This error can occur when you are not using a RunAs account or the RunAs account has expired. See ["Manage Azure Automation RunAs accounts"](https://docs.microsoft.com/azure/automation/manage-runas-account).

### "Run Login-AzureRmAccount to login"

* This error can occur when you are not using a RunAs account or the RunAs account has expired. See ["Manage Azure Automation RunAs accounts"](https://docs.microsoft.com/azure/automation/manage-runas-account).

### Runbook fails with error "Strong authentication enrollment is required"

* See ["Authentication to Azure failed because multi-factor authentication is enabled" in the Runbook troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#auth-failed-mfa)

### Runbook fails with "No permission" or some variation

* RunAs accounts may not have the same permissions against Azure resources as your current account. Ensure your RunAs account [has permissions to access any resources](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) used in your script.

### "Command not recognized"

* This error is commonly caused when modules have not been imported or are otherwise out of date. Ensure any dependent modules in your script have been [imported into Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-gallery#modules-in-powershell-gallery) and are the correct version. If the module exists in your Automation Account already, there might be an issue with loading it in the sandbox. You can try adding an explicit Import-Module statement to the beginning of your runbook. 

### "Forbidden with client authentication scheme "anonymous""

* This error occurs when using credentials inside of an Azure Automation sandbox. Please use the -ServicePrincipal parameter on any Azure resources with the RunAs account. 

### "Unable to require token for tenant XXX-XXX-XXX-XXX"

* This error occurs when using credentials inside of an Azure Automation sandbox. Please use the -ServicePrincipal parameter on any Azure resources with the RunAs account. 

### "Server failed to authenticate the request"

* This error occurs when using credentials inside of an Azure Automation sandbox. Please use the -ServicePrincipal parameter on any Azure resources with the RunAs account. 

### Error: "429: The request rate is currently too large. Please try again"

* See the ["Request rate too large" section of the Runbook troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#429)

### Runbooks were working, but suddenly stopped

* If runbooks were previously executing but stopped, [ensure the RunAs account has not expired](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)
* If you are using webhooks to start runbooks, [ensure the webhook has not expired](https://docs.microsoft.com/azure/automation/automation-webhooks#renew-webhook)

### Using a Hybrid Worker

* If you are using a hybrid worker to execute jobs, please consult the [Hybrid Runbook Worker troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker)

### Using Az modules

* Using Az modules and AzureRM modules in the same Automation Account is not supported. Please see ["Az modules in runbooks" for more details](https://docs.microsoft.com/azure/automation/automation-update-azure-modules).

### Runbook is stuck

* If you are unable to stop a runbook job in the portal, you may be able to stop it via PowerShell with either [Stop-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Stop-AzureRmAutomationJob?view=azurermps-6.13.0) or [Stop-AzAutomationJob](https://docs.microsoft.com/powershell/module/az.automation/Stop-AzAutomationJob?view=azps-2.4.0)

### Can't start or schedule runbook

* Ensure your runbook [is in the Published state](https://docs.microsoft.com/azure/automation/manage-runbooks#publish-a-runbook).

### Using cmdlets that depend on binaries

* Some cmdlets may rely on binaries, such as Microsoft Data Access Components (MDAC) or the Azure Fabric SDK. These cmdlets can not be run inside of the Azure Automation sandbox and need to be executed via [a hybrid worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). 

### Dealing with multiple subscriptions inside of a runbook

* If you need to manage Azure resources across several subscriptions with Azure Automation, please follow the guidance in ["Dealing with Multiple Subscriptions"](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#runbook-auth-failure) to prevent errors

If none of the above solutions address your problem, please follow the steps in [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case) before opening a case. This will help us resolve your case as quickly as possible.

## **Recommended Documents**

* [Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
* [Starting a Runbook in Azure Automation](https://docs.microsoft.com/azure/automation/automation-starting-a-runbook)
* [Runbook Execution in Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-execution)
