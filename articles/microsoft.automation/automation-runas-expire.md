<properties
  pagetitle="Azure Automation: expired or expiring Run As accounts "
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="riyadav"
  selfhelptype="Generic"
  supporttopicids="32628007,32628011,32635010,32635015,32782940"
  resourcetags=""
  productpesids="15607"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="fbf1c295-d499-4593-bfa9-c41bf607f19c"
  ownershipid="Compute_Automation" />
# Azure Automation: expired or expiring Run As accounts 
The Self-Signed certificate created for Run As/Classic Run As account expires one year from date of creation. 

## **Recommended Steps**

### **1. Check permissions required to renew or recreate Run As/Classic Run As account**
To manage Run As/Classic Run As accounts, you will need permissions. See [Permissions Required to Manage Run As/Classic Run As Accounts](https://docs.microsoft.com/azure/automation/automation-security-overview#permissions)

### **2. Renew a Self-Signed Certificate**
Before your Run As/Classic Run As certificate expires, you can renew it by following the [Certificate Renewal Instructions](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)

### **3. Re-create a Run As/Classic Run As Account**
After your Run As/Classic Run As certificate expires, you must delete it and create a new one. Follow the instructions to [Delete](https://docs.microsoft.com/azure/automation/delete-run-as-account) and [Re-create](https://docs.microsoft.com/azure/automation/create-run-as-account) an Azure Run As/Classic Run As account.

## Troubleshoot issues with Run As accounts
If you are not able to renew or re-create Run As/Classic Run As account by following the steps above, see the following sections.

### **Run As/Classic Run As accounts are greyed out**
Run As and Classic Run As accounts appear dimmed when you do not have sufficient permissions. Check out the [Permissions required to Manage Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/automation-security-overview#permissions).

### **Create a Run As/Classic Run As account related to Start/Stop VMs**
See [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management) for information on permissions needed to create Run As/Classic Run As accounts related to the Start/Stop solution

## **Recommended Documents**

* [Resolve a Misconfigured/Incomplete Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#resolve-misconfiguration-issues-for-run-as-accounts)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
