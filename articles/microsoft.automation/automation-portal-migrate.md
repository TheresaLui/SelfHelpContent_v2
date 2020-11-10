<properties
    pageTitle="Azure Automation - Migrating Automation Account"
    description="Azure Automation - Migrating Automation Account"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599921"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="c910835b-0cc1-4936-bc5c-c32327edba50"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Migrating Automation Account
The Automation Account is used to host a variety of services, from runbooks to Update Management and Start-Stop VM Solution. This article will help you troubleshoot specific aspects of creating and maintaining an Automation Account.

## **Recommended Steps**

### **I want to move my Automation Account to another subscription**

See the document ["Move your automation account to another subscription"](https://docs.microsoft.com/azure/automation/how-to/move-account)

### **"Classic RunAs account is about to expire"**

See the document ["Manage Azure Automation Run-As account"](https://docs.microsoft.com/azure/automation/manage-runas-account). If you are not using Classic resources it is safe to [delete the AzureClassicRunAsCertificate resource](https://docs.microsoft.com/azure/automation/manage-runas-account#delete-a-run-as-or-classic-run-as-account).  


## **Recommended Documents**

* [Azure Automation documentation](https://docs.microsoft.com/azure/automation/)<br>
* [Quickstart create Automation account](https://docs.microsoft.com/azure/automation/automation-quickstart-create-account)<br>
* [Create standalone Automation account](https://docs.microsoft.com/azure/automation/automation-create-standalone-account)<br>
* [Automation billing](https://docs.microsoft.com/azure/automation/automation-intro#pricing-for-automation)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
