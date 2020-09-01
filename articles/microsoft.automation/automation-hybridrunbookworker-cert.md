<properties
    pageTitle="Azure Automation - Hybrid Runbook and Certificates"
    description="Azure Automation - Hybrid Runbook and Certificates"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599940"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="164e8d47-b5be-41b4-99df-6058f60bd770"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Using Hybrid Runbook Worker with RunAs

## **Recommended Steps**

Many issues with Hybrid Workers are caused by connectivity problems. Run [the "Test Cloud Connectivity" tool](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows-troubleshoot#connectivity-issues) to ensure your environment is properly configured. 

### Authenticating against Azure Resources from Hybrid Worker

* Runbooks from a hybrid worker behave differently from runbooks in an Azure Automation sandbox. The article ["Runbook Permissions"](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks#runbook-permissions) explains how authentication works for different runbook environments. 


### No certificate was found in the certificate store

* To resolve this issue, follow the ["No Certificate was Found" section of the Hybrid Worker troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found)

### Error: "Machine is already registered to a different account"

* Follow the troubleshooting guide for ["Unable to add a Hybrid Runbook Worker"](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#already-registered)


## **Recommended Documents**

* [Automation Hybrid Runbook Workers](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker)<br>
* [Deploy Windows Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-windows-hrw-install)<br>
* [Deploy Linux Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-linux-hrw-install)<br>
* [Run runbooks on Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
