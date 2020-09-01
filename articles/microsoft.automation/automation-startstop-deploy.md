<properties
    pageTitle="Azure Automation - Deploy Start-Stop"
    description="Azure Automation - Deploy Start-Stop"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32615223"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="200cd370-6c98-4260-a76e-c70c72be9dee"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Problem Deploying Start-Stop Solution
If you are trying to deploy the [Start/Stop VMs solution](https://docs.microsoft.com/azure/automation/automation-solution-vm-management), but it isn't working, please refer to the steps below.

## **Recommended Steps**

### **Start/Stop Solution won't deploy**

* Ensure you have an [Azure Automation RunAs account](https://docs.microsoft.com/azure/automation/manage-runas-account)
* Review the [deployment documentation for Start-Stop VM Solution](https://docs.microsoft.com/azure/automation/automation-solution-vm-management#deploy-the-solution)
* Try creating a new automation account just for the Start-Stop VM solution
* Review the ["Fails to properly deploy" section of the Start/Stop Troubleshooting Guide](https://docs.microsoft.com/azure/automation/troubleshoot/start-stop-vm#deployment-failure)

### **"resourceGroupName' does not match the expected pattern"**

* This is caused by an older version of the Start/Stop VM Solution. Follow the ["Update the Solution" guide](https://docs.microsoft.com/azure/automation/automation-solution-vm-management#update-the-solution).  

### **Error: "A parameter cannot be found that matches parameter name 'TagName'."**

* This error is caused by having an outdated version of the AzureRM modules or an outdated Start/Stop solution. To resolve, [follow the instructions to re-deploy the solution](https://docs.microsoft.com/azure/automation/automation-solution-vm-management#update-the-solution).

## **Recommended Documents**

* [Start-Stop VM Troubleshooting Guide](https://docs.microsoft.com/azure/automation/troubleshoot/start-stop-vm#other)

