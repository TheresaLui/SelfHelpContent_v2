<properties
  pagetitle="Azure Automation - Creating Run As Accounts "
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="riyadav"
  selfhelptype="Generic"
  supporttopicids="32635009"
  resourcetags=""
  productpesids="15607"
  cloudenvironments="fairfax,mooncake,public,usnat,ussec,blackforest"
  disableclouds=""
  articleid="279cadce-7e06-46bf-a70a-f0268a71a9be"
  ownershipid="Compute_Automation" />
# Azure Automation - Creating Run As Accounts 
Run As accounts are used by Azure Automation to help authenticate against Azure resources.

## **Recommended Steps**

### **What is Run As account and Types of Run As account**
To get started with the concept of Run As account and Types of Run As account, see [Run As account Overview](https://docs.microsoft.com/azure/automation/automation-security-overview#run-as-accounts)

### **Permissions Required for Run As/Classic Run As account**
To create and manage a Run As/Classic Run As account, you need certain permissions. See [Permissions required to manage Run As account](https://docs.microsoft.com/azure/automation/automation-security-overview#permissions)

### **How to Create a Run As/Classic Run As account**
* To create a Run As/Classic Run As account in Azure Portal, follow step-by-step instructions to [create a Run As/Classic Run As account in Azure portal](https://docs.microsoft.com/azure/automation/create-run-as-account#create-account-in-azure-portal)
* To create a Run As/Classic Run As account using PowerShell, follow step-by-step instructions to [create a Run As/Classic Run As account using PowerShell](https://docs.microsoft.com/azure/automation/create-run-as-account#create-account-using-powershell)

### **How to Delete a Run As/Classic Run As account**
Follow step-by-step instructions to [delete a Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/delete-run-as-account)

### **How to Renew a Run As/Classic Run As account Certificate**
The Self-signed certificate created for Run As account expires one year from date of creation. Renew it any time before it expires by following the steps in [Run As/Classic Run As account Certificate Renewal](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)

### **Using Run As account with Hybrid Worker**
You might see the error message, "No certificate was found in the certificate store". To resolve this issue, see the ["No Certificate was Found" section of the Hybrid Worker troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found)

## **Recommended Documents**

* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
