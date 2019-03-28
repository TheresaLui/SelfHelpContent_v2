<properties
    pageTitle="Azure Stack Diagnostics and Performance Counters"
    description="Resolve issue with Azure Stack Diagnostics and Performance Counters"
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

# Resolve issue with Azure Stack Diagnostics and Performance Counters

Azure Stack provides many of the same tools as Azure public cloud for VM diagnostics. 

**Azure Monitor for VMs** monitors your Azure and Azure Stack virtual machines (VM) and virtual machine scale sets at scale. It analyzes the performance and health of your Windows and Linux VMs, and monitors their processes and dependencies on other resources and external processes.

**Azure Diagnostics Extension** helps you configure the VM to collect diagnostics data that can be used to monitor the health of your application.

## Recommended Steps

- To view default diagnostic information of a specific VM, select the VM in the Azure Stack portal, choose Diagnostic settings, and select the metrics you wish to track
- To see more granular and VM-specific metrics, you need to [install the Azure diagnostics extension](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-monitoring#install-diagnostics-extension) on the VM, by clicking the *Enable guest-level monitoring button*
- As Windows virtual machines boot up, the [boot diagnostic agent](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) captures screen output that can be used for troubleshooting purposes
- To monitor sets of VMs across Azure and Azure Stack, [enable Azure Monitor for VMs running on Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/vm-update-management#enable-azure-monitor-for-vms-running-on-azure-stack)
- Review [supported metrics with Azure Monitor on Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-metrics-supported) and then retrieve metrics from Azure monitor using the same steps as in Azure

## **Recommended Documents**

- [What is Azure Diagnostics extension](https://docs.microsoft.com/azure/monitoring-and-diagnostics/azure-diagnostics).
- [Azure Monitor on Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-metrics-azure-data)
- [Extensions on Azure Stack VMs](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-compute-overview#extensions)
- [Tutorial: Monitor and update a Windows virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-monitoring)