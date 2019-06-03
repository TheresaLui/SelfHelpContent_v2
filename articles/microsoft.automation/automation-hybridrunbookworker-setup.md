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
    cloudEnvironments="public"
	articleId="700a5b2b-7aec-4816-bb4f-4cd60893b2c3"
/>

# Azure Automation - Setup Hybrid Runbook Worker

## **Recommended Steps**

### **Ensure the agent is present** 

* For **Linux**, ensure the agent is running by following the [Linux OMS Agent troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#oms-agent-not-running)
* For **Windows**, ensure the agent is running by following the [Windows MMA troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#mma-not-running)

### **Error: Job action 'Activate' cannot be run...**

* See the [hybrid runbook worker troubleshooting guide under "Runbook execution fails"](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#runbook-execution-fails)

### **No certificate was found in the certificate store**

* To resolve this issue, follow the ["No Certificate was Found" section of the Hybrid Worker troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#no-cert-found)

### **Error: "Machine is already registered to a different account"**

* Follow the troubleshooting guide for ["Unable to add a Hybrid Runbook Worker"](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#already-registered)


## **Recommended Documents**

* [Automation Hybrid Runbook Workers](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker)<br>
* [Deploy Windows Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-windows-hrw-install)<br>
* [Deploy Linux Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-linux-hrw-install)<br>
* [Run runbooks on Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks)<br>
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
