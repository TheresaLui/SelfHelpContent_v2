<properties
  pagetitle="Azure Automation: expired or expiring Run As accounts &#xD;"
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="riyadav"
  selfhelptype="Generic"
  supporttopicids="32628007,32628011"
  resourcetags=""
  productpesids="15607"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="fbf1c295-d499-4593-bfa9-c41bf607f19c"
  ownershipid="Compute_Automation" />
# Azure Automation: expired or expiring Run As accounts 

The Self-Signed certificate created for Run As/Classic Run As account **expires 1 year from date of creation** and **must be renewed before the expiration date**. The user can extend the validity of the certificate by 1 year any time before the certificate expires. If you miss renewing it before the expiration date, your runbooks that use Run As account for authentication to Azure resources will fail. However, if you miss renewing, you can renew it even after it has expired.

**Note**: Renewing the Run As account certificate is **free, at no additional cost**. Also, when you renew the Run As account certificate, the current certificate is retained to ensure that **the runbooks that are running or queued up aren’t affected due to the renewal process**, provided it is renewed before the expiration date. Therefore, you can go ahead and renew your Run As account certificate without worrying about any impact on your runbooks.
 
## **Recommended Steps**

1. **Check the permissions required to renew or re-create Run As/Classic Run As account**<br>
   To manage Run As/Classic Run As accounts, you need permissions. See [Permissions Required to Manage Run As/Classic Run As Accounts](https://docs.microsoft.com/azure/automation/automation-security-overview#permissions).

2. **Renew a Self-Signed Certificate**<br>
   Before your Run As/Classic Run As certificate expires, you can renew it by following the [Certificate Renewal Instructions](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal). If you miss renewing the Run As certificate before the expiration date, you can still renew it using the same method mentioned above.

## Troubleshoot issues with Run As accounts
If you are unable to renew or re-create Run As/Classic Run As accounts by following the preceding steps, see the following sections.

### **Run As/Classic Run As accounts are grayed out**
Run As and Classic Run As accounts appear grayed out when you don't have sufficient permissions. See [Permissions required to Manage Run As/Classic Run As account](https://docs.microsoft.com/azure/automation/automation-security-overview#permissions).

### **Create a Run As/Classic Run As account related to Start/Stop VMs**
For information on permissions needed to create Run As/Classic Run As accounts related to the Start/Stop solution, see [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management). 

## **Recommended Documents**

* [Introduction to Run As account - 4-minute video](https://www.microsoft.com/videoplayer/embed/RWwtF3)
* [Resolve a misconfigured or incomplete Run As account](https://docs.microsoft.com/azure/automation/manage-runas-account#resolve-misconfiguration-issues-for-run-as-accounts)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
