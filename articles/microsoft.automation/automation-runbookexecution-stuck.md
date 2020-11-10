<properties
    pageTitle="Stuck Runbook Job in Azure Automation"
    description="Stuck Runbook Job in Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32628013"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="51343bcc-ad63-4e52-aeaf-e0e0188cd049"
	ownershipId="Compute_Automation"
/>

# Runbook Job Stuck in Azure Automation

This article discusses how to handle a job that will not stop running or otherwise change state in Azure Automation.

## **Recommended Steps**

### **Runbook is stuck**

* If you are unable to stop a runbook job in the portal, you may be able to stop it via PowerShell with either [Stop-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Stop-AzureRmAutomationJob?view=azurermps-6.13.0) or [Stop-AzAutomationJob](https://docs.microsoft.com/powershell/module/az.automation/Stop-AzAutomationJob?view=azps-2.4.0)

### **Runbook is suspended or unexpectedly failed**

There are several reasons why a runbook may be suspended or failed:

* [Job Statuses](https://docs.microsoft.com/azure/automation/automation-runbook-execution#job-statuses) defines runbook statuses and some possible causes
* [Add additional output](https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#message-streams) to the runbook to identify what happens before the runbook is suspended
* [Handle any exceptions](https://docs.microsoft.com/azure/automation/automation-runbook-execution#handling-exceptions) that are thrown by your job

### **Job was tried three times but it failed**

* Check the [Automation Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits), and consider moving to a [Hybrid Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker) if the limitation applies to Azure sandboxes only

### **Runbooks were working, but suddenly stopped**

* If runbooks were previously executing but stopped, [ensure the RunAs account has not expired](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)
* If you are using webhooks to start runbooks, [ensure the webhook has not expired](https://docs.microsoft.com/azure/automation/automation-webhooks#renew-webhook).


If none of the above solutions address your problem, please follow the steps in [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case) before opening a case. This will help us resolve your case as quickly as possible.


## **Recommended Documents**

* [Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
* [Starting a Runbook in Azure Automation](https://docs.microsoft.com/azure/automation/automation-starting-a-runbook)
* [Runbook Execution in Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-execution)
