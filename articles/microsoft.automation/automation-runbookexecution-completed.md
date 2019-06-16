<properties
    pageTitle="Troubleshoot Runbook Execution in Azure Automation"
    description="Troubleshoot Runbook Execution in Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599907"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public"
    articleId="746842a1-a2f1-44fe-b43c-3ea53a470bb5"
/>

# Troubleshoot Runbook Execution in Azure Automation - Job Completed With Errors

Here are some common issues with executing runbooks in Azure Automation and how to address them. Please note that Support will not write a new script for you based on your needs, but we will work with you to ensure your existing script executes correctly inside of Azure Automation. 

## **Recommended Steps**

Specific problems and their solutions are listed below, but we highly recommend you try these two troubleshooting steps first:

* Try running the [runbook locally](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#runbook-fails) before running it in Azure Automation. This can clarify if the issue is a bug in the runbook versus an issue with Azure Automation.
* [Add additional output](https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#message-streams) to the runbook to identify where the error occurs 

### Inconsistent behavior in runbooks

* Follow the guidance in [Runbook Execution](https://docs.microsoft.com/azure/automation/automation-runbook-execution#runbook-behavior) to avoid issues with concurrent jobs, resources getting created multiple times, or other timing-sensitive logic in runbooks. 

### Switching between multiple subscriptions in a runbook

* Follow the guidance in "Working with multiple subscriptions"(https://docs.microsoft.com/azure/automation/automation-runbook-execution#working-with-multiple-subscriptions)

### Runbooks were working, but suddenly stopped

* If runbooks were previously executing but stopped, [ensure the RunAs account has not expired](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)
* If you are using webhooks to start runbooks, [ensure the webhook has not expired](https://docs.microsoft.com/azure/automation/automation-webhooks#renew-webhook).

### Passing parameters into webhooks

* For help passing parameters into webhooks, see [Start a runbook from a webhook](https://docs.microsoft.com/azure/automation/automation-webhooks#parameters)

### Using Az modules

* Using Az modules and AzureRM modules in the same Automation Account is not supported. Please see ["Az modules in runbooks" for more details](https://docs.microsoft.com/azure/automation/az-modules).

If none of the above solutions address your problem, please follow the steps in [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510) before opening a case. This will help us resolve your case as quickly as possible.

## **Recommended Documents**

* [Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
* [Starting a Runbook in Azure Automation](https://docs.microsoft.com/azure/automation/automation-starting-a-runbook)
* [Runbook Execution in Azure Automation](https://docs.microsoft.com/azure/automation/automation-runbook-execution)
