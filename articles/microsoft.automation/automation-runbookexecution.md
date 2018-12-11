<properties
    pageTitle="Azure Automation - Runbook Execution"
    description="Azure Automation - Runbook Execution"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    authorAlias="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599860,32599923,32599906,32599907,32599908,32599909,32615224,32628014,32628013"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public"
/>

# Azure Automation - Runbook Execution
Here are some common issues with executing runbooks in Azure Automation and how to address them.

## **Recommended Steps**

Specific problems and their solutions are listed below, but we highly recommend you try these two troubleshooting steps first:

* Try running the runbook locally before running it in Azure Automation. This can clarify if the issue is a bug in the runbook versus an issue with Azure Automation
* [Update the Azure PowerShell](https://docs.microsoft.com/azure/automation/automation-update-azure-modules) modules in your Automation Account to the latest version

1. **Runbook fails with "The subscription cannot be found"**

This issue can occur when the runbook isn't using a RunAs account to access Azure resources. To resolve, follow the steps in [Scenario: Unable to find the Azure subscription](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#unable-to-find-subscription) 

2. **Runbook is suspended or unexpectedly failed**

There are several reasons why a runbook may be suspended or failed:

* [Job Statuses](https://docs.microsoft.com/azure/automation/automation-runbook-execution#job-statuses) defines runbook statuses and some possible causes
* [Add additional output](https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#message-streams) to the runbook to identify what happens before the runbook is suspended
* Check [Automation Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits), and consider moving to a [Hybrid Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker) if the limitation applies to Azure sandboxes only

3. **Hybrid runbook worker doesn't run jobs or isn't responding**

If you are running jobs using a hybrid worker instead of in Azure Automation, you might need to troubleshoot the hybrid worker itself:

* [Troubleshoot runbooks in hybrid runbook workers](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker)<br>
<br>

If none of the above solutions address your problem, please follow the steps in [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510) before opening a case. This will help us resolve your case as quickly as possible. 

## **Recommended Documents** ##
* [Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
* [Starting a Runbook in Azure Automation](https://docs.microsoft.com/azure/automation/automation-starting-a-runbook)
* [Runbook Execution in Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-execution)

