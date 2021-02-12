<properties
    pageTitle="Azure Automation - VMs Don't Start/Stop"
    description="Azure Automation - VMs Don't Start/Stop"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32635008"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8924af8e-96f5-4373-b030-6da407049d44"
	ownershipId="Compute_Automation"
/>

# Azure Automation - All VMs fail to start or stop
Here are some common issues which might cause all VMs to start or stop.
If you have an issue where some, but not all, VMs will not start or stop on schedule, please choose "Some VMs fail to start or stop" as your category to see more relevant information. 

## **Recommended Steps**


### **Start/Stop VM has been configured, but it doesn't start/stop all the VMs**

* Please refer to the ["All VMs fail to Start/Stop" section of the Start/Stop VM Troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/start-stop-vm#all-vms-fail-to-startstop)

### **Error: "A parameter cannot be found that matches parameter name 'TagName'."**

* This error is caused by having an outdated version of the AzureRM modules or an outdated Start/Stop solution. To resolve, [follow the instructions to re-deploy the solution](https://docs.microsoft.com/azure/automation/automation-solution-vm-management#update-the-solution). 


## **Recommended Documents** ##

* [Deployment documentation for Start-Stop VM Solution](https://docs.microsoft.com/azure/automation/automation-solution-vm-management#deploy-the-solution)
* [Start/Stop VM Troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/start-stop-vm#issue)

