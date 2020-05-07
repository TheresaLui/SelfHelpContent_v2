<properties
    pageTitle="Azure Automation - Python Runbook Development"
    description="Azure Automation - Python Runbook Development"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599904"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="7a6acd2a-6109-49dc-96cd-55c2e9842aa6"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Python Runbook Development
Here are some common issues when creating new runbooks for use with Azure Automation.

## **Recommended Steps**

Specific problems and their solutions are listed below, but we highly recommend you try these this first:

* Try [executing the runbook locally](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#runbook-fails) before running it in Azure Automation. This can clarify if the issue is a bug in the runbook versus an issue with Azure Automation.

* Remember to [add authentication to manage Azure Resources](https://docs.microsoft.com/azure/automation/automation-first-runbook-textual-python2#add-authentication-to-manage-azure-resources) 

**Using webhooks with Python**

* As per [the Python runbook documentation](https://docs.microsoft.com/azure/automation/automation-first-runbook-textual-python2), using a webhook to start a Python runbook is not supported

**Using input parameters with Python**

* See ["Use input parameters"](https://docs.microsoft.com/azure/automation/automation-first-runbook-textual-python2#use-input-parameters)

**Using Python2 Packages in a runbook**

* See the ["Python Packages" document](https://docs.microsoft.com/azure/automation/python-packages#use-a-package-in-a-runbook)
## **Recommended Documents**

* [Troubleshoot errors with runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)<br>
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
