<properties
  pagetitle="Azure Automation - Creating Automation Account"
  description="Azure Automation - Creating Automation Account"
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="riyadav"
  selfhelptype="Generic"
  supporttopicids="32599929"
  resourcetags=""
  productpesids="15607"
  cloudenvironments="fairfax,mooncake,public,usnat,ussec,blackforest"
  disableclouds=""
  articleid="628c7a60-1534-4fe0-9f5a-5a125a45772a"
  ownershipid="Compute_Automation" />
# Azure Automation - Creating Automation Account

The Automation Account hosts a variety of services, from runbooks to Update Management and Start/Stop VM Solutions. This article can help you troubleshoot specific aspects of creating and maintaining an Automation Account.

## **Recommended Steps**

### **Steps to create an Automation account**

* Follow the steps mentioned [here](https://docs.microsoft.com/azure/automation/automation-create-standalone-account) to create an Automation account.

### **I want to know what regions Automation Accounts are available in**

* This information can be found at [the **Azure Products by Region** page](https://azure.microsoft.com/global-infrastructure/services/?products=automation&regions=all). This page also includes information about planned future availability.
* Automation Accounts can manage resources in any region, regardless of the region the account is created in.

### **I am having trouble selecting a Log Analytics workspace**

* When enabling solutions, only certain regions are supported for linking a Log Analytics workspace and an Automation Account. See [Supported Region mappings](https://docs.microsoft.com/azure/automation/how-to/region-mappings#supported-mappings)

### **I'm having trouble creating an Automation Account**

* When creating an Automation Account, the most common issue is permissions. Review [Permissions required to Create an Automation Account](https://docs.microsoft.com/azure/automation/automation-create-standalone-account#permissions-required-to-create-an-automation-account)

### **I can't create or renew a RunAs account / RunAs is not available**

* RunAs and Classic RunAs accounts are dimmed when you do not have sufficient permissions. You might also see the message "You do not have permissions to create…"
* Review [*Unable to Update or Create RunAs account* in the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/shared-resources#unable-create-update) 

### **Managing permissions and access**

* Review the document [Role based access control in Azure Automation](https://docs.microsoft.com/azure/automation/automation-role-based-access-control)

### **I want to start/stop VMs on a schedule**

* Review [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management)

### **Unable to register Automation Resource Provider**

* Review [Unable to register Automation Resource Provider](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#rp-register)


## **Recommended Documents**

* [Azure Automation documentation](https://docs.microsoft.com/azure/automation/)<br>
* [Quickstart create Automation account](https://docs.microsoft.com/azure/automation/automation-quickstart-create-account)<br>
* [Create standalone Automation account](https://docs.microsoft.com/azure/automation/automation-create-standalone-account)<br>
* [Automation billing](https://docs.microsoft.com/azure/automation/automation-intro#pricing-for-automation)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
