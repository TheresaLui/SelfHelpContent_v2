<properties
    pageTitle="Azure Automation - Automation Account"
    description="Azure Automation - Automation Account"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599858"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="1266529a-8bfb-4011-ab4d-071691bdf78a"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Automation Account
The Automation Account is used to host a variety of services, from runbooks to Update Management and Start-Stop VM Solution. This article will help you troubleshoot specific aspects of creating and maintaining an Automation Account.

## **Recommended Steps**

### **I want to know what regions Automation Accounts are available in**

* This information can be found at [the "Azure Products by Region" page](https://azure.microsoft.com/global-infrastructure/services/?products=automation&regions=all). This page also includes information about planned future availability

### **I'm having trouble creating an Automation Account**

* The most common issues creating an Automation Account are related to permissions. Check ["Permissions required to Create an Automation Account"](https://docs.microsoft.com/azure/automation/automation-create-standalone-account#permissions-required-to-create-an-automation-account)

### **I can't create or renew a RunAs account / RunAs is greyed out**

* RunAs and Classic RunAs accounts are greyed out when you do not have sufficient permissions. You might also see the message "You do not have permissions to create…"
* See the ["Unable to Update or Create RunAs account"section of the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/shared-resources#unable-create-update) 

### **Deleting an Automation Account**

* If you are trying and failing to delete an Automation Account, please ensure all workspaces are unlinked by following the instructions at ["Unlink a Workspace"](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-browse#unlink-workspace)


## **Recommended Documents**

* [Azure Automation documentation](https://docs.microsoft.com/azure/automation/)<br>
* [Quickstart create Automation account](https://docs.microsoft.com/azure/automation/automation-quickstart-create-account)<br>
* [Create standalone Automation account](https://docs.microsoft.com/azure/automation/automation-create-standalone-account)<br>
* [Automation billing](https://docs.microsoft.com/azure/automation/automation-intro#pricing-for-automation)<br>
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
