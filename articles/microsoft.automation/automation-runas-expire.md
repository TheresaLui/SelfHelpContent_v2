<properties
    pageTitle="Azure Automation - Expired Run As Accounts"
    description="Azure Automation - Expired Run As Accounts"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32628007, 32628010, 32628011, 32635010,32635015"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="fbf1c295-d499-4593-bfa9-c41bf607f19c"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Expired or Expiring Run As Accounts 
RunAs accounts are used by Azure Automation to help authenticate against Azure resources.

## **Recommended Steps**

In order to manage RunAs accounts, you will need permissions as listed at ["Permissions Required to Manage RunAs Accounts"](https://docs.microsoft.com/azure/automation/manage-runas-account#permissions)

### Renewing self-signed certificate

* Before your RunAs certificate expires, you can renew it by following the Cert Renewal instructions at ["Manage RunAs Accounts"](https://docs.microsoft.com/azure/automation/manage-runas-account#cert-renewal).

### Recreating RunAs Account

* After your RunAs certificate expires, you will have to delete it and create a new one by following the instructions for ["Delete and recreate an Azure RunAs account"](https://docs.microsoft.com/azure/automation/manage-runas-account#delete-a-run-as-or-classic-run-as-account)

### I want to start/stop VMs

* See [Start/Stop VMs during off-hours](https://docs.microsoft.com/azure/automation/automation-solution-vm-management) for information on permissions needed to create RunAs accounts related to the Start/Stop solution


## **Recommended Documents**

* [Misconfigured Run As account](https://docs.microsoft.com/azure/automation/automation-manage-account#misconfiguration)<br>
* [Run As account certificate renewal](https://docs.microsoft.com/azure/automation/automation-manage-account#self-signed-certificate-renewal)<br>
* [Create and manage Run As account](https://docs.microsoft.com/azure/automation/automation-create-runas-account)<br>
* [Test Run As account authentication](https://docs.microsoft.com/azure/automation/automation-verify-runas-authentication)<br>
* [Delete a Run As account](https://docs.microsoft.com/azure/automation/automation-manage-account#delete-a-run-as-or-classic-run-as-account)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
