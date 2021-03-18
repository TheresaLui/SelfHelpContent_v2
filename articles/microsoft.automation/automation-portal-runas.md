<properties
  pagetitle="Azure Automation: Issues with creating Run As accounts&#xD;"
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="riyadav"
  selfhelptype="Generic"
  supporttopicids="32628010,32642189"
  resourcetags=""
  productpesids="15607"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="b1d09aaa-7185-44ab-999c-b51d64b77a75"
  ownershipid="Compute_Automation" />
# Azure Automation: Issues with creating Run As accounts

Most users can resolve common issues with creating a Run As account by using the following information. 

* **Run As/Classic Run As accounts are unavailable or grayed out**
   
   If you don't have sufficient permissions, Run As and Classic Run As accounts appear grayed out. To create or update a Run As account, make sure that you have the [permissions required to create a Run As or Classic Run As account](https://docs.microsoft.com/azure/automation/automation-security-overview#permissions).

* **Error message: "You do not have permissions to create.."**
   
   If you receive this error when you try to create or update a Run As account, see the ["Unable to Update or Create Run As account" section of the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/shared-resources#unable-create-update).

* **Renewing a Run As/Classic Run As Account that is about to expire or has already expired**
   
   When your Run As/Classic Run As certificate is about to expire or has already expired, you can renew it by following the [Certificate Renewal Instructions](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal).

* **Issues while creating Run As/Classic Run As account to Start/Stop VM**
   
  For information on permissions needed to create Run As accounts related to the Start/Stop solution, see [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management).

* **Using Run As account with Hybrid Worker**
   
   If you see the error message, "No certificate was found in the certificate store," you can resolve the issue by following steps in the ["No Certificate was Found" section of the Hybrid Worker troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found).


## **Recommended Documents**

* [**4-minute video** - Introduction to Run As account](https://www.microsoft.com/videoplayer/embed/RWwtF3)
* [Create a Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/create-run-as-account)<br>
* [Delete a Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/delete-run-as-account)<br>
* [Run As/Classic Run As account certificate renewal](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal)<br>
* [Resolve a Misconfigured/Incomplete Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#resolve-misconfiguration-issues-for-run-as-accounts)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
