<properties
    pageTitle="Azure Automation - Hybrid Runbook Worker Setup"
    description="Azure Automation - Hybrid Runbook Worker Setup"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599939"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="700a5b2b-7aec-4816-bb4f-4cd60893b2c3"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Setup Hybrid Runbook Worker

## **Recommended Steps**

Many issues with Hybrid Workers are caused by connectivity problems. Run [the "Test Cloud Connectivity" tool](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows-troubleshoot#connectivity-issues) to ensure your environment is properly configured. 

You can run the [offline version of the Agent Registration script](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) to find more detailed troubleshooting on prerequisites for the Hybrid Worker. Although this script performs some checks related to Update Management, most requirements are the same for hybrid workers. 

### **Ensure the agent is present** 

* For **Linux**, ensure the agent is running by following the [Linux OMS Agent troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#oms-agent-not-running)
* For **Windows**, ensure the agent is running by following the [Windows MMA troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#mma-not-running)

### **Error: Job action 'Activate' cannot be run...**

* See the [hybrid runbook worker troubleshooting guide under "Runbook execution fails"](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#runbook-execution-fails)

### **No certificate was found in the certificate store**

* To resolve this issue, follow the ["No Certificate was Found" section of the Hybrid Worker troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found)

### **Error: "Machine is already registered"**

* Follow the troubleshooting guide for ["Unable to add a Hybrid Runbook Worker"](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#already-registered)

### **"Last seen time" not updated**

* If the hybrid worker isn't reporting to the Azure Automation service, follow the [Troubleshoot Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker) guide for your OS
* Review the [network planning guide](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker#network-planning) and ensure you have connectivity to the service

## **Recommended Documents**

* [Automation Hybrid Runbook Workers](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker)<br>
* [Deploy Windows Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-windows-hrw-install)<br>
* [Deploy Linux Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-linux-hrw-install)<br>
* [Run runbooks on Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
