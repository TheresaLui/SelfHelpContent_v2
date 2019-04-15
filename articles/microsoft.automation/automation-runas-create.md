<properties
    pageTitle="Azure Automation - Creating Run As Accounts"
    description="Azure Automation - Creating Run As Accounts"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32635007,32635009"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public"
	articleId="279cadce-7e06-46bf-a70a-f0268a71a9be"
/>

# Azure Automation - Creating Run As Accounts 
RunAs accounts are used by Azure Automation to help authenticate against Azure resources.

## **Recommended Steps**

In order to manage RunAs accounts, you will need permissions as listed at ["Permissions Required to Manage RunAs Accounts"](https://docs.microsoft.com/azure/automation/manage-runas-account#permissions)

### I can't create or renew a RunAs account / RunAs is greyed out

* RunAs and Classic RunAs accounts are greyed out when you do not have sufficient permissions
* You might also see the message "You do not have permissions to create…"
* See the ["Unable to Update or Create RunAs account" section of the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/shared-resources#unable-create-update) 


## **Recommended Documents**

* [Misconfigured Run As account](https://docs.microsoft.com/azure/automation/automation-manage-account#misconfiguration)<br>
* [Run As account certificate renewal](https://docs.microsoft.com/azure/automation/automation-manage-account#self-signed-certificate-renewal)<br>
* [Create and manage Run As account](https://docs.microsoft.com/azure/automation/automation-create-runas-account)<br>
* [Test Run As account authentication](https://docs.microsoft.com/azure/automation/automation-verify-runas-authentication)<br>
* [Delete a Run As account](https://docs.microsoft.com/azure/automation/automation-manage-account#delete-a-run-as-or-classic-run-as-account)<br>
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
