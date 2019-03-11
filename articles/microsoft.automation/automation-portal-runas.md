<properties
    pageTitle="Azure Automation - Run As Accounts"
    description="Azure Automation - Run As Accounts"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32628004,32628007,32628010,32628011"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public"
	articleId="b1d09aaa-7185-44ab-999c-b51d64b77a75"
/>

# Azure Automation - Run As Accounts
RunAs accounts are used by Azure Automation to help authenticate against Azure resources.

## **Recommended Steps**

### I can't create or renew a RunAs account / RunAs is greyed out

* RunAs and Classic RunAs accounts are greyed out when you do not have sufficient permissions
* You might also see the message "You do not have permissions to create…"
* See the ["Unable to Update or Create RunAs account"section of the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/shared-resources#unable-create-update) 

### Using RunAs with a Hybrid Worker

* You might see the error "No certificate was found in the certificate store"
* To resolve this issue, follow the ["No Certificate was Found" section of the Hybrid Worker troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found)

## **Recommended Documents**

* [Misconfigured Run As account](https://docs.microsoft.com/azure/automation/automation-manage-account#misconfiguration)<br>
* [Run As account certificate renewal](https://docs.microsoft.com/azure/automation/automation-manage-account#self-signed-certificate-renewal)<br>
* [Create and manage Run As account](https://docs.microsoft.com/azure/automation/automation-create-runas-account)<br>
* [Test Run As account authentication](https://docs.microsoft.com/azure/automation/automation-verify-runas-authentication)<br>
* [Delete a Run As account](https://docs.microsoft.com/azure/automation/automation-manage-account#delete-a-run-as-or-classic-run-as-account)<br>
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
