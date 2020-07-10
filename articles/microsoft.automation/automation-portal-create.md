<properties
    pageTitle="Azure Automation - Creating Automation Account"
    description="Azure Automation - Creating Automation Account"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599929"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="628c7a60-1534-4fe0-9f5a-5a125a45772a"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Creating Automation Account
The Automation Account is used to host a variety of services, from runbooks to Update Management and Start-Stop VM Solution. This article will help you troubleshoot specific aspects of creating and maintaining an Automation Account.

## **Recommended Steps**

### **I want to know what regions Automation Accounts are available in**

* This information can be found at [the "Azure Products by Region" page](https://azure.microsoft.com/global-infrastructure/services/?products=automation&regions=all). This page also includes information about planned future availability.
* Note that Automation Accounts can manage resources in any region, regardless of the region the account is created in.

### **I am having trouble selecting a Log Analytics workspace**

* When enabling solutions, only certain regions are supported for linking a Log Analytics workspace and an Automation Account. See ["Enable Solutions" for the supported region mappings](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#enable-solutions)

### **I'm having trouble creating an Automation Account**

* The most common issues creating an Automation Account are related to permissions. Check ["Permissions required to Create an Automation Account"](https://docs.microsoft.com/azure/automation/automation-create-standalone-account#permissions-required-to-create-an-automation-account)

### **I can't create or renew a RunAs account / RunAs is greyed out**

* RunAs and Classic RunAs accounts are greyed out when you do not have sufficient permissions. You might also see the message "You do not have permissions to create…"
* See the ["Unable to Update or Create RunAs account"section of the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/shared-resources#unable-create-update) 

### **Managing permissions and access**

* See the document ["Role based access control in Azure Automation"](https://docs.microsoft.com/azure/automation/automation-role-based-access-control)

### **I want to start/stop VMs on a schedule**

* See [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management)

### **"Unable to register Automation Resource Provider"**

* See ["Unable to register Automation Resource Provider"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#rp-register)


## **Recommended Documents**

* [Azure Automation documentation](https://docs.microsoft.com/azure/automation/)<br>
* [Quickstart create Automation account](https://docs.microsoft.com/azure/automation/automation-quickstart-create-account)<br>
* [Create standalone Automation account](https://docs.microsoft.com/azure/automation/automation-create-standalone-account)<br>
* [Automation billing](https://docs.microsoft.com/azure/automation/automation-intro#pricing-for-automation)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
