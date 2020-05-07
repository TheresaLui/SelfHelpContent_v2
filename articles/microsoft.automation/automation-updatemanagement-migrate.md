<properties
    pageTitle="Migrate machines in Update Management"
    description="Migrate machines in Update Management"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32642185"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="29dd1252-32be-46ca-b717-475d33300501"
	ownershipId="Compute_Automation"
/>

# Move my Update Management machines to another subscription

This article will help you migrate your Update Management account or VMs to another subscription. 

## **Recommended Steps**

### **Move Automation Accounts**

* To move Automation Accounts, see ["How to Move Azure Automation accounts"](https://docs.microsoft.com/azure/automation/how-to/move-account)

### **Move machine from Update Management**

* First, [unenroll machines from Update Management](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-browse#clean-up-resources)
* Then, [onboard machines to a different account](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#enable-solutions)

### **Desired automation account, region, or Log Analytics workspace is greyed out**

* Only certain regions are supported for linking Log Analytics and Automation Accounts, which is required for Update Management. See the ["Workspace Mappings"](https://docs.microsoft.com/azure/automation/how-to/region-mappings) document for the full list of supported regions.

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
