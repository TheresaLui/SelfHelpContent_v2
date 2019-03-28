<properties
    pageTitle="Azure Stack Diagnostics and Performance Counters"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629206"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-vm-diagnostics"
/>

# Azure Stack Diagnostics and Performance Counters

You can monitor your compute resources, such as VMs, or resources on our VMs.<br>

## Azure Monitor to check compute health

You can retrieve your metrics from Azure monitor on Azure Stack in the same as global Azure. You can create your measures in the portal, get them from the REST API, or query them with PowerShell or CLI.<br>

For the monitors for compute on Azure Stack, see [Microsoft.Compute/virtualMachines](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-metrics-supported#microsoftcomputevirtualmachines).<br>

## Diagnostics extensions to monitor app health

The Azure Diagnostics Extension helps you configure the VM to collect diagnostics data that can be used to monitor the health of your application.<br>

The Azure Diagnostics extension is an agent within Azure that enables the collection of diagnostic data on a deployed application. You can use the diagnostics extension from a number of different sources. Currently supported are Azure Cloud Service (classic) Web and Worker Roles, Virtual Machines, Virtual Machine Scale sets, and Service Fabric.<br>

For more information on Azure Diagnostics extension, see [What is Azure Diagnostics extension](https://docs.microsoft.com/azure/monitoring-and-diagnostics/azure-diagnostics).<br>

## **Recommended documents**

[Extensions on Azure Stack VMs](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-compute-overview#extensions)<br>
[Azure Monitor on Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/user/azure-stack-metrics-azure-data)<br>
[Tutorial: Monitor and update a Windows virtual machine in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/tutorial-monitoring)