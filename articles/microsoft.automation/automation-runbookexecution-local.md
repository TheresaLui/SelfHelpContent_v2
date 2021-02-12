<properties
    pageTitle="Troubleshoot Runbook Execution in Azure Automation"
    description="Troubleshoot Runbook Execution in Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder="202"
    selfHelpType="generic"
    supportTopicIds="32635012"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="29c081cb-767b-442c-8c84-2ddec8d54e75"
	ownershipId="Compute_Automation"
/>

# Troubleshoot Runbook Execution in Azure Automation - Runbook works locally, but not in Automation

Here are some common issues with executing runbooks in Azure Automation and how to address them. Please note that Support will not write a new script for you based on your needs, but we will work with you to ensure your existing script executes correctly inside of Azure Automation. 

## **Recommended Steps**

Specific problems and steps to resolve them follow, but first review ["My Runbook fails but works when ran locally"](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#runbook-fails) in the troubleshooting guide. 

### **Runbook fails with "The subscription cannot be found" error**

* This issue can occur when the runbook isn't using a RunAs account to access Azure resources. To resolve, follow the steps in [Scenario: Unable to find the Azure subscription](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#unable-to-find-subscription).

### **Runbook fails with error "Strong authentication enrollment is required"**

* See ["Authentication to Azure failed because multi-factor authentication is enabled" in the Runbook troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#auth-failed-mfa)

### **Runbook fails with "No permission" or some variation**

* RunAs accounts may not have the same permissions against Azure resources as your current account. Ensure your RunAs account [has permissions to access any resources](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) used in your script.

### **Runbook is suspended or unexpectedly failed**

There are several reasons why a runbook may be suspended or failed:

* [Job Statuses](https://docs.microsoft.com/azure/automation/automation-runbook-execution#job-statuses) defines runbook statuses and some possible causes
* [Add additional output](https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#message-streams) to the runbook to identify what happens before the runbook is suspended
* If you receive the error "The job was tried three times but it failed", check [Automation Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits), and consider moving to a [Hybrid Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker) if the limitation applies to Azure sandboxes only

### **Error: "429: The request rate is currently too large. Please try again"**

* See the ["Request rate too large" section of the Runbook troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#429)

### **Hybrid runbook worker doesn't run jobs or isn't responding**

* If you are running jobs using a hybrid worker instead of in Azure Automation, you might need to [troubleshoot the hybrid worker](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker) itself

### **Runbooks were working, but suddenly stopped**

* If runbooks were previously executing but stopped, [ensure the RunAs account has not expired](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)
* If you are using webhooks to start runbooks, [ensure the webhook has not expired](https://docs.microsoft.com/azure/automation/automation-webhooks#renew-webhook)

### **Passing parameters into webhooks**

* For help passing parameters into webhooks, see [Start a runbook from a webhook](https://docs.microsoft.com/azure/automation/automation-webhooks#parameters)

### **Using Az modules**

* Using Az modules and AzureRM modules in the same Automation Account is not supported. Please see ["Az modules in runbooks" for more details](https://docs.microsoft.com/azure/automation/automation-update-azure-modules).

### **Can't start or schedule runbook**

* Ensure your runbook [is in the Published state](https://docs.microsoft.com/azure/automation/manage-runbooks#publish-a-runbook).

If none of the above solutions address your problem, please follow the steps in [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case) before opening a case. This will help us resolve your case as quickly as possible.

## **Recommended Documents**

* [Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
* [Starting a Runbook in Azure Automation](https://docs.microsoft.com/azure/automation/automation-starting-a-runbook)
* [Runbook Execution in Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-execution)
