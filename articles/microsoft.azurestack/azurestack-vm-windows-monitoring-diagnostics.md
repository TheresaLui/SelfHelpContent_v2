<properties
    pageTitle="Azure Stack Windows VM monitoring and diagnostics issues"
    description="Azure Stack Windows VM monitoring and diagnostics issues"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="genlin"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663912"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6f641910-1006-4135-b8d1-85ab25fa1503"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Windows VM monitoring and diagnostics issues

Azure Stack provides many of the same tools as Azure public cloud for VM diagnostics. **Azure Diagnostics Extension** helps you configure the VM to collect diagnostics data that can be used to monitor the health of your application. **Azure Monitor for VMs** monitors your Azure and Azure Stack virtual machines (VM) and virtual machine scale sets at scale. It analyzes the performance and health of your Windows VMs, and monitors their processes and dependencies on other resources and external processes.

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

- To view diagnostic information for a specific VM, select the VM in the Azure Stack portal, choose Diagnostic settings, and select the metrics you wish to track
- For more granular and VM-specific metrics, you need to [install the Azure diagnostics extension](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-monitoring#install-diagnostics-extension) on the VM, by clicking the Enable guest-level monitoring button
- When a VM boots up, the [boot diagnostic agent](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) captures screen output that can be used for troubleshooting purposes in the portal
- To monitor sets of VMs across Azure and Azure Stack, [enable Azure Monitor for VMs running on Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/vm-update-management#enable-azure-monitor-for-vms-running-on-azure-stack)
- Review [supported metrics with Azure Monitor on Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-metrics-supported), and then retrieve metrics from [Azure Monitor for VMs](https://docs.microsoft.com/azure/azure-monitor/overview#azure-monitor-for-vms) in the public portal

## **Recommended Documents**

- [What is Azure Diagnostics extension](https://docs.microsoft.com/azure/monitoring-and-diagnostics/azure-diagnostics)
- [Azure Monitor on Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-metrics-azure-data)
- [Prerequisites for Azure Monitor on Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-metrics-azure-data#prerequisites-for-azure-monitor-on-azure-stack)
- [Extensions on Azure Stack VMs](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-compute-overview#extensions)
- [Tutorial: Monitor and update a Windows VM in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-monitoring)
