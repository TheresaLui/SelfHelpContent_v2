<properties
    pageTitle="Azure Automation - Hybrid Runbook Worker"
    description="Azure Automation - Hybrid Runbook Worker"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder="301"
    selfHelpType="generic"
    supportTopicIds="32628014,32599920"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="b3d96b2b-2651-474d-b08d-a1a28b66f86d"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Hybrid Runbook Worker

## **Recommended Steps**

Many issues with Hybrid Workers are caused by connectivity problems. Run [the "Test Cloud Connectivity" tool](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows-troubleshoot#connectivity-issues) to ensure your environment is properly configured. 

### **Ensure the agent is present** 

* For **Linux**, ensure the agent is running by following the [Linux OMS Agent troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#oms-agent-not-running)
* For **Windows**, ensure the agent is running by following the [Windows MMA troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#mma-not-running)

### **Error: Job action 'Activate' cannot be run...**

* See the [hybrid runbook worker troubleshooting guide under "Runbook execution fails"](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#runbook-execution-fails)

### **No certificate was found in the certificate store**

* To resolve this issue, follow the ["No Certificate was Found" section of the Hybrid Worker troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found)

### **Authenticating against Azure resources from a Hybrid Worker**

* You can avoid using a RunAs account with a Hybrid Worker by using Managed Identities
* For more details, see [Managed Identities for Azure Resources](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks#managed-identities-for-azure-resources)

### **Differences between Hybrid Runbook Worker and Azure sandbox**

* Azure sandbox has [several internal cmdlets which are not available in the Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/shared-resources/modules#internal-cmdlets)
* When running in a hybrid runbook worker, you can use the equivalent [AzureRM](https://docs.microsoft.com/powershell/module/azurerm.automation/) or [Az](https://docs.microsoft.com/powershell/module/az.automation) cmdlets
* Hybrid Worker does not have access to your Automation account modules. [See "Install PowerShell modules"](https://docs.microsoft.com/azure/automation/automation-windows-hrw-install#5-install-powershell-modules)

### **Error: "Machine is already registered to a different account"**

* Follow the troubleshooting guide for ["Unable to add a Hybrid Runbook Worker"](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#already-registered)

### **Can't start or schedule runbook**

* Ensure your runbook [is in the Published state](https://docs.microsoft.com/azure/automation/manage-runbooks#publish-a-runbook).


## **Recommended Documents**

* [Automation Hybrid Runbook Workers](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker)<br>
* [Deploy Windows Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-windows-hrw-install)<br>
* [Deploy Linux Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-linux-hrw-install)<br>
* [Run runbooks on Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
