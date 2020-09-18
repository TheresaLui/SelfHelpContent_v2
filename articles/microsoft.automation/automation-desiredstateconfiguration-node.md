<properties
    pageTitle="Azure Automation - State Configuration (DSC) - Node"
    description="Azure Automation - State Configuration (DSC)"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32627997"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f97563fd-0f5c-4f44-81ef-bc9bb5f48ba6"
	ownershipId="Compute_Automation"
/>

# Azure Automation - State Configuration (DSC) - Node Configuration Fails

## **Recommended Steps**

* For issues on a machine, [collect diagnostic logs](https://docs.microsoft.com/azure/automation/troubleshoot/desired-state-configuration#steps-to-troubleshoot-desired-state-configuration-dsc)

### **"Provisioning failed"**

* Most issues are caused by network configurations. Please review the requirements in the [Prerequisites section of the State Configuration overview](https://docs.microsoft.com/azure/automation/automation-dsc-overview#network-planning).

### **Node is in "Failed" status with "Not Found" error**

* Review the ["Node is in failed status" section of the State Configuration troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/desired-state-configuration#failed-not-found)

### **Stuck "in progress"**

* Review the ["DSC node report becomes stuck 'in progress' state" section of the State Configuration troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/desired-state-configuration#dsc-in-progress)

### **"One or more errors occurred"**

* If you are using Register-AzAutomationDscNode or Register-AzureRMAutomationDscNode and receiving this error, it is because the resource can't be found
* This can often occur when trying to onboard nodes across subscriptions. To achieve this, follow the documentation at ["Onboarding Machines for Management"](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions).

### **Checking error logs**

* See ["Using xDscDiagnostics to Analyze DSC Logs"](https://docs.microsoft.com/powershell/scripting/dsc/troubleshooting/troubleshooting?view=powershell-5.1#using-xdscdiagnostics-to-analyze-dsc-logs) for information on how to collect logs Support will need to help you with your case.
* You can also [follow the "Using DSC Logs to diagnose script errors" guide](https://docs.microsoft.com/powershell/scripting/dsc/troubleshooting/troubleshooting?view=powershell-5.1#my-script-wont-run-using-dsc-logs-to-diagnose-script-errors)

### **Import-DscResource: Could not find the module**

* You must upload modules included in your DSC configuration to the automation account. See [Adding required DSC resources to Pull Server](https://docs.microsoft.com/azure/automation/automation-dsc-cd-chocolatey#step-3-adding-required-dsc-resources-to-the-pull-server).

### **DSC and VMSS**

* To deploy DSC with VMSS, consult the sample template ["VMSS Configuration managed by Azure Automation"](https://azure.microsoft.com/resources/templates/201-vmss-automation-dsc/)

### **Issues with a specific DSC Resource**

* For support with specific DSC resources, you will need to file an issue with the resource owner. Many resources can be found [on GitHub in the DSC Resources repository](https://github.com/PowerShell/DscResources#dsc-resources). 

## **Recommended Documents**

* [Troubleshoot issues with Automation DSC](https://docs.microsoft.com/azure/automation/troubleshoot/desired-state-configuration)<br>
* [Automation State Configuration (DSC) QuickStart](https://docs.microsoft.com/azure/automation/automation-quickstart-dsc-configuration)<br>
* [Automation DSC Overview](https://docs.microsoft.com/azure/automation/automation-dsc-overview)<br>
* [Getting Started with Automation DSC](https://docs.microsoft.com/azure/automation/automation-dsc-getting-started) <br>
* [Videos on how to setup Automation DSC](https://channel9.msdn.com/Blogs/MVP-Azure/Azure-Automation-DSC-Part-1-Introduction) <br>
* [Onboarding machines to Automation DSC](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding)<br>
* [Configure servers to a desired state](https://docs.microsoft.com/azure/automation/tutorial-configure-servers-desired-state) <br>
* [Compiling Configurations in Automation DSC](https://docs.microsoft.com/azure/automation/automation-dsc-compile) <br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
