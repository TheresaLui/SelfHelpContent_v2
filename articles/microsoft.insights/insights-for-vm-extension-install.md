<properties
     pageTitle="I cannot get the VM extensions to install on my Azure VM"
    description="I cannot get the VM extensions to install on my Azure VM"
    infoBubbleText="Here are some things to help with installing the extensions"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-extension-install-Azurevm"
    productPesIds="17081"
    supportTopicIds="32738506"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

 

# I cannot get the VM extensions to install on my Azure VM

Azure Monitor for VMs installs two virtual machine extensions on an Azure virtual machine.  The Log Analytics agent and the Dependency agent virtual machine extensions.  Both need to be installed and configured properly for the monitoring data to be collected to support our monitoring views. 

## **Recommended Steps**

### **Azure Virtual Machines**

If you used the onboarding method in the Azure portal to enable monitoring on the VM, then it handles the installation of the extensions for you automatically.  If this is failing, make sure that you are [using a supported operating system](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-enable-overview#supported-operating-systems) on the VM.   

Also, the process of installing the extensions on the VM is handled by the Microsoft Azure Virtual Machine Agent (VM Agent).  This agent may need to be updated or installed if it is not present.  Review this article about the [Linux VMs](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-linux) and [Windows VMs](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows). 

If the agent extensions fail to install, you can choose to remove them and perform the onboarding process again to see if this resolves the issue. 

In some cases, very small VMs (Size B for example) can have such limited resources that they can fail during extension installation. To address this, try using a larger VM size with more resources. 
 
### **Azure Virtual Machine Scale Sets**

The process for installing the extension on a VM scale set is similar to the process for installing it onto an Azure virtual machine. In this case, the extension is added to the scale set model definition.  If it is failing to install, verify that your OS is supported and that you are not running a very small VM size for pilot testing (Size B VM for example). 

Once installed to the scale set model definition, you then need to push those changes from the model out to the instances that are running in the scale set.  This can be done manually if needed.  If the scale set model is using rolling or automatic updates it will happen automatically. 

### **On-premise or other machines**

Extensions are only provided for Azure resources and are not applicable for on-premise physical or virtual machines.  Follow our [onboarding process for hybrid monitoring](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-enable-hybrid-cloud) to enable monitoring on these resources. 

We do have plans to offer extension support for on-premise and other cloud VMs managed as [Azure Arc servers](https://azure.microsoft.com/services/azure-arc/).
 
