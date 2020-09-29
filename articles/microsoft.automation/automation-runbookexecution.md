<properties
    pageTitle="Troubleshoot Runbook Execution in Azure Automation"
    description="Troubleshoot Runbook Execution in Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32642190"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e633b59d-0baf-4a33-8caf-e135f3d246cd"
	ownershipId="Compute_Automation"
/>

# Troubleshoot Runbook Execution in Azure Automation

Here are some common issues with executing runbooks in Azure Automation and how to address them. Please note that Support will not write a new script for you based on your needs, but we will work with you to ensure your existing script executes correctly inside of Azure Automation. 

## **Recommended Steps**

Specific problems and their solutions are listed below, but we highly recommend you try these two troubleshooting steps first:

* Try running the [runbook locally](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#runbook-fails) before running it in Azure Automation. This can clarify if the issue is a bug in the runbook versus an issue with Azure Automation.
* Investigate runbook [error streams](https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#runbook-output) for specific messages and compare them to the errors below. 
* [Update the Azure PowerShell](https://docs.microsoft.com/azure/automation/automation-update-azure-modules) modules in your Automation Account to the latest version

### Runbook fails with "The subscription cannot be found" error

This issue can occur when the runbook isn't using a RunAs account to access Azure resources. To resolve, follow the steps in [Scenario: Unable to find the Azure subscription](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#unable-to-find-subscription).

### "Run Login-AzureRmAccount to login"

* This error can occur when you are not using a RunAs account or the RunAs account has expired. See ["Manage Azure Automation RunAs accounts"](https://docs.microsoft.com/azure/automation/manage-runas-account).

### Runbook fails with error "Strong authentication enrollment is required"

* See ["Authentication to Azure failed because multi-factor authentication is enabled" in the Runbook troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#auth-failed-mfa)

### Runbook fails with "No permission" or some variation

* RunAs accounts may not have the same permissions against Azure resources as your current account. Ensure your RunAs account [has permissions to access any resources](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) used in your script.

### Runbook is suspended or unexpectedly failed

There are several reasons why a runbook may be suspended or failed:

* [Job Statuses](https://docs.microsoft.com/azure/automation/automation-runbook-execution#job-statuses) defines runbook statuses and some possible causes
* [Add additional output](https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#message-streams) to the runbook to identify what happens before the runbook is suspended
* If you receive the error "The job was tried three times but it failed", check [Automation Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits), and consider moving to a [Hybrid Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker) if the limitation applies to Azure sandboxes only

### Error: "429: The request rate is currently too large. Please try again"

* See the ["Request rate too large" section of the Runbook troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#429)

### Hybrid runbook worker doesn't run jobs or isn't responding

If you are running jobs using a hybrid worker instead of in Azure Automation, you might need to troubleshoot the hybrid worker itself:

* [Troubleshoot runbooks in hybrid runbook workers](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker)

### Runbooks were working, but suddenly stopped

* If runbooks were previously executing but stopped, [ensure the RunAs account has not expired](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)
* If you are using webhooks to start runbooks, [ensure the webhook has not expired](https://docs.microsoft.com/azure/automation/automation-webhooks#renew-webhook).

### Passing parameters into webhooks

* For help passing parameters into webhooks, see [Start a runbook from a webhook](https://docs.microsoft.com/azure/automation/automation-webhooks#parameters)

### Using Az modules

* Using Az modules and AzureRM modules in the same Automation Account is not supported. Please see ["Az modules in runbooks" for more details](https://docs.microsoft.com/azure/automation/automation-update-azure-modules).

If none of the above solutions address your problem, please follow the steps in [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case) before opening a case. This will help us resolve your case as quickly as possible.

## **Recommended Documents**

* [Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
* [Starting a Runbook in Azure Automation](https://docs.microsoft.com/azure/automation/automation-starting-a-runbook)
* [Runbook Execution in Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-execution)
