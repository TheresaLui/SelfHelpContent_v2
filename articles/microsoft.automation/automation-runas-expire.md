<properties
  pagetitle="Azure Automation - Expired or Expiring Run As Accounts &#xD;"
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="riyadav"
  selfhelptype="Generic"
  supporttopicids="32628007,32628011,32635010,32635015,32782940"
  resourcetags=""
  productpesids="15607"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="fbf1c295-d499-4593-bfa9-c41bf607f19c"
  ownershipid="Compute_Automation" />
# Azure Automation: expired or expiring Run As accounts 
The Self-Signed certificate created for Run As/Classic Run As account expires one year from date of creation. 

## **Recommended Steps**

### **Check permissions required to renew or recreate Run As/Classic Run As account**

* In order to manage Run As/Classic Run As accounts, you will need permissions. See [Permissions Required to Manage Run As/Classic Run As Accounts](https://docs.microsoft.com/azure/automation/manage-runas-account#permissions)

### **Renew a Self-Signed Certificate**

* Before your Run As/Classic Run As certificate expires, you can renew it by following the [Certificate Renewal Instructions](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)

### **Re-create a Run As/Classic Run As Account**

* After your Run As/Classic Run As certificate expires, you must delete it and create a new one by following the instructions to [Delete and Re-create an Azure Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#delete-a-run-as-or-classic-run-as-account)

If you are not able to renew or re-create Run As/Classic Run As account by following the steps above, see the following sections.

### **Access Run As/Classic Run As accounts**

* Run As and Classic Run As accounts are unavailable when you do not have sufficient permissions. Check out the [Permissions required to Manage Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#permissions)

### **Create a Run As/Classic Run As account related to Start/Stop VMs**

* See [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management) for information on permissions needed to create Run As/Classic Run As accounts related to the Start/Stop solution

## **Recommended Documents**
* [Create and manage Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#create-a-run-as-account-in-azure-portal)<br>
* [Delete a Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#delete-a-run-as-or-classic-run-as-account)<br>
* [Run As/Classic Run As account certificate renewal](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)<br>
* [Resolve a Misconfigured/Incomplete Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#resolve-misconfiguration-issues-for-run-as-accounts)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
