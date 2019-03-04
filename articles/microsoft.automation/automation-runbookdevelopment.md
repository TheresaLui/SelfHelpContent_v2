<properties
    pageTitle="Azure Automation - Runbook Development"
    description="Azure Automation - Runbook Development"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599859,32599862,32599904,32599905,32599922,32628016,32628015"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public"
	articleId="03905ebe-c243-4c0d-ad0f-f33720a11133"
/>

# Azure Automation - Runbook Development
Here are some common issues when creating new runbooks for use with Azure Automation.

## **Recommended Steps**

Specific problems and their solutions are listed below, but we highly recommend you try these this first:

* Try running the runbook locally before running it in Azure Automation. This can clarify if the issue is a bug in the runbook versus an issue with Azure Automation. See ["My runbook fails but works when run locally" ](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#runbook-fails)

**Runbook fails with "Command not found" or "Cannot bind parameter" message**

* You may need to [update the Azure modules in your automation account](https://docs.microsoft.com/azure/automation/automation-update-azure-modules).
* If running locally or on a hybrid worker, ensure the machine running the scripts has the same modules versions as your Automation Account by running Get-Module -ListAvailable 

**Runbook fails with "The subscription cannot be found"**

* This issue can occur when the runbook isn't using a RunAs account to access Azure resources. To resolve, follow the steps in [Scenario: Unable to find the Azure subscription](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#unable-to-find-subscription). 

**Runbook fails with error "Strong authentication enrollment is required"**

* See ["Authentication to Azure failed because milt-factor authentication is enabled" in the Runbook troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#auth-failed-mfa)

**"Your azure credentials have not been set up or have expired, please run connect-azureRmAccount to set up your azure credentials"**

* This error can occur when you are not using a RunAs account or the RunAs account has expired. See ["Manage Azure Automation RunAs accounts"](https://docs.microsoft.com/azure/automation/manage-runas-account)

**Runbook fails with "No permission" or some variation**

* RunAs accounts may not have the same permissions against Azure resources as your current account. Ensure your RunAs account [has permissions to access any resources](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) used in your script. 


## **Recommended documents**
* Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)<br>
<br>
* [Automation runbook types](https://docs.microsoft.com/azure/automation/automation-runbook-types)<br>
* [Creating or importing a runbook](https://docs.microsoft.com/azure/automation/automation-creating-importing-runbook)<br>
* [Quickstart create a runbook](https://docs.microsoft.com/azure/automation/automation-quickstart-create-runbook)<br>
* [Starting an Azure Automation runbook with a webhook](https://docs.microsoft.com/azure/automation/automation-webhooks)<br>
* [Runbook and module galleries for Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-gallery)<br>
<br>
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)