<properties
  pagetitle="Azure Automation - Run As Accounts"
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="riyadav"
  selfhelptype="Generic"
  supporttopicids="32635018,32635011,32642189"
  resourcetags=""
  productpesids="15607"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="b1d09aaa-7185-44ab-999c-b51d64b77a75"
  ownershipid="Compute_Automation" />
# Azure Automation - Run As Accounts

## **Recommended Steps**

### **Check Permissions required to create Run As/Classic Run As account**
In order to create or update a Run As account, you need certain permissions. See [permissions Required to Create Run As/Classic Run As Account](https://docs.microsoft.com/azure/automation/manage-runas-account#permissions)

If this is not an issue for you, see the following sections to find a solution to your specific issue.

### **Other Possible Issues**

### **Run As/Classic Run As account grayed out**
* Run As and Classic Run As accounts are grayed out when you do not have sufficient permissions. See [permissions required to Create and Manage Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#permissions) 

### **"You do not have permissions to create.." error message**
* When you try to create or update a Run As account, you may receive this error. See the ["Unable to Update or Create Run As account" section of the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/shared-resources#unable-create-update)

### **Recreating Run As/Classic Run As Account which has expired**
* After your Run As/Classic Run As certificate expires, you will have to delete it and create a new one. See [deleting and recreating an Azure Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#delete-a-run-as-or-classic-run-as-account)

### **Issues while creating Run As/Classic Run As account to Start/Stop VM**
* See [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management) for information on permissions needed to create Run As accounts related to the Start/Stop solution

### **Using Run As account with Hybrid Worker**
* You might see the error message, "No certificate was found in the certificate store". To resolve this issue, follow the ["No Certificate was Found" section of the Hybrid Worker troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found)

## **Recommended Documents**

* [Create and manage Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#create-a-run-as-account-in-azure-portal)<br>
* [Delete a Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#delete-a-run-as-or-classic-run-as-account)<br>
* [Run As/Classic Run As account certificate renewal](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)<br>
* [Resolve a Misconfigured/Incomplete Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#resolve-misconfiguration-issues-for-run-as-accounts)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
