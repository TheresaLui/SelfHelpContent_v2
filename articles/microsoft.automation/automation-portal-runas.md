<properties
  pagetitle="Azure Automation: Common issues with Run As accounts"
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="riyadav"
  selfhelptype="Generic"
  supporttopicids="32628010,32635018,32642189"
  resourcetags=""
  productpesids="15607"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="b1d09aaa-7185-44ab-999c-b51d64b77a75"
  ownershipid="Compute_Automation" />
# Azure Automation: Common issues with Run As accounts

This article provides resources to help you resolve common issues with Run As accounts. 

* **Run As/Classic Run As accounts are unavailable**
   
   If you do not have sufficient permissions, Run As and Classic Run As accounts appear dimmed. To create or update a Run As account, make sure that you have the [permissions required to create a Run As or Classic Run As account](https://docs.microsoft.com/azure/automation/automation-security-overview#permissions).

* **Error: "You do not have permissions to create.."**
   
   If you receive this error when you try to create or update a Run As account, see the ["Unable to Update or Create Run As account" section of the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/shared-resources#unable-create-update).

* **Recreating a Run As/Classic Run As Account that has expired**
   
   When your Run As/Classic Run As certificate expires, you must delete it and create a new one. See instructions to [delete](https://docs.microsoft.com/azure/automation/delete-run-as-account) and [re-create](https://docs.microsoft.com/azure/automation/create-run-as-account) an Azure Run As/Classic Run As account.

* **Issues while creating Run As/Classic Run As account to Start/Stop VM**
   
   See [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management) for information on permissions needed to create Run As accounts related to the Start/Stop solution

* **Using Run As account with Hybrid Worker**
   
   You might see the error, "No certificate was found in the certificate store". To resolve this issue, follow the ["No Certificate was Found" section of the Hybrid Worker troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found).


## **Recommended Documents**

* [Create a Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/create-run-as-account)<br>
* [Delete a Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/delete-run-as-account)<br>
* [Run As/Classic Run As account certificate renewal](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)<br>
* [Resolve a Misconfigured/Incomplete Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#resolve-misconfiguration-issues-for-run-as-accounts)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
