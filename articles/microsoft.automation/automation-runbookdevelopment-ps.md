<properties
    pageTitle="Azure Automation - PowerShell Runbook Development"
    description="Azure Automation - PowerShell Runbook Development"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599862"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="c1ad5dbf-f48c-478e-843a-fa63a3977cc6"
	ownershipId="Compute_Automation"
/>

# Azure Automation - PowerShell Runbook Development
Here are some common issues when creating new runbooks for use with Azure Automation. Please note that Support will not write a new script for you based on your needs, but we will work with you to ensure your existing script executes correctly inside of Azure Automation. 

## **Recommended Steps**

Specific problems and their solutions are listed below, but we highly recommend you try these this first:

* Try [executing the runbook locally](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#runbook-fails) before running it in Azure Automation. This can clarify if the issue is a bug in the runbook versus an issue with Azure Automation.

* Remember to [add authentication to manage Azure Resources](https://docs.microsoft.com/azure/automation/automation-first-runbook-textual-powershell#add-authentication-to-manage-azure-resources) 

* Review the [known issues of PowerShell runbooks](https://docs.microsoft.com/azure/automation/automation-runbook-types#known-issues)

* Review [how to handle exceptions and errors in a PowerShell runbook](https://docs.microsoft.com/azure/automation/automation-runbook-execution#handling-exceptions)

**Runbook fails with "Command not found" or "Cannot bind parameter" message**

* You may need to [update the Azure modules in your automation account](https://docs.microsoft.com/azure/automation/automation-update-azure-modules)
* If running locally or on a hybrid worker, ensure the machine running the scripts has the same modules versions as your Automation Account by running `Get-Module -ListAvailable`

**Runbook fails with error "The subscription cannot be found"**

* This issue can occur when the runbook isn't using a RunAs account to access Azure resources. To resolve, follow the steps in [Scenario: Unable to find the Azure subscription](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#unable-to-find-subscription). 

**Runbook fails with error "Strong authentication enrollment is required"**

* See ["Authentication to Azure failed because multi-factor authentication is enabled" in the Runbook troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#auth-failed-mfa)

**"Your azure credentials have not been set up or have expired, please run connect-azureRmAccount to set up your azure credentials"**

* This error can occur when you are not using a RunAs account or the RunAs account has expired. See ["Manage Azure Automation RunAs accounts"](https://docs.microsoft.com/azure/automation/manage-runas-account).

**Runbook fails with "No permission" or some variation**

* RunAs accounts may not have the same permissions against Azure resources as your current account. Ensure your RunAs account [has permissions to access any resources](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) used in your script. 

**Errors about "TypeData"**

* If you are receiving errors about TypeData, you are running a PowerShell Workflow with modules that do not support Workflow. You need to change the runbook type to PowerShell. See ["Runbook types" for more details](https://docs.microsoft.com/azure/automation/automation-runbook-types#powershell-runbooks).

## **Recommended Documents**

* Guidance on [runbook authoring best practices](https://docs.microsoft.com/azure/automation/automation-runbook-execution#runbook-behavior)<br>
* [Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)<br>
* [Starting a Runbook in Azure Automation](https://docs.microsoft.com/azure/automation/automation-starting-a-runbook)
