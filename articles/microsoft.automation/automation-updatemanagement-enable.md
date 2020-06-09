<properties
    pageTitle="Issues enabling Update Management"
    description="Troubleshoot issues enabling Update Management"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder="101"
    selfHelpType="generic"
    supportTopicIds="32599903"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e7641147-7a28-4ba4-ba37-49ee74bc9637"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation - Enabling Update Management

This article will help with several kinds of issues relating to enabling the Azure Update Management solution.

## **Recommended Steps**

The Update Agent Troubleshooter ([Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues), [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux)) will detect common issues such as restrictive firewalls, missing prerequisites, or misconfigured registry keys. 

### **Desired automation account, region, or Log Analytics workspace is greyed out**

* Only certain regions are supported for linking Log Analytics and Automation Accounts, which is required for Update Management. See the ["Workspace Mappings"](https://docs.microsoft.com/azure/automation/how-to/region-mappings) document for the full list of supported regions.
* If your region is not listed as a supported region, you can [file a feedback request on our UserVoice](https://feedback.azure.com/forums/905242-update-management)

### **Permissions needed to enable and use Update Management**

* The ["Role-Based Access Control" guide](https://docs.microsoft.com/azure/automation/automation-role-based-access-control#update-management) has a list of necessary permissions for enabling and using Update Management

### **Machine isn't onboarding after waiting 15 minutes**

* The ["Components enabled but not working" section of the Update Management Troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#components-enabled-not-working) covers common issues such as:
  * Cloned machines or machines with the same name in the same Log Analytics workspace
  * Network endpoints are inaccessible
  * Scope configuration prevents machines from receiving the Update Management solution

### **The solution cannot be enabled on this VM because the VM already has the management agent..."**

* This error occurs when a machine is already reporting to a different Log Analytics workspace
* A common cause is when [Azure Security Center](https://docs.microsoft.com/azure/security-center/) already manages a machine

## **Recommended Documents**

* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Automate onboarding Update Management](https://docs.microsoft.com/azure/cloud-adoption-framework/manage/azure-server-management/onboarding-automation)
* [Update Management Overview - Supported Clients, Permissions and Network Requirements](https://docs.microsoft.com/azure/automation/automation-update-management)
