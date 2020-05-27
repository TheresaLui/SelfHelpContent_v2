<properties
     pageTitle="I see a message about monitoring data being collected, but the data is never displayed"
    description="I see a message about monitoring data being collected, but the data is never   displayed"
    infoBubbleText="Here are some things to help with getting data to display"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-data-not-displayed"
    productPesIds="17081"
    supportTopicIds="32738514"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

# I see a message about monitoring data being collected, but the data is never displayed

Are you seeing a message about monitoring data being collected and that it can take 10 minutes or so to arrive?  Still seeing this message hours or days later? 

Occasionally the VM can be slow to recognize that the extensions have been installed.  Generally though, this means something went wrong with the extension installation and startup.   

## **Recommended Steps**

### **First thing to check**

Is the VM running?  If the VM has been turned off for a while, is off currently, or was only recently turned on then you won't have data to display for a bit until data arrives. 

### **Second thing to check** 

Is the operating system on the VM supported?  If it is not in our [list of supported operating systems](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-enable-overview#supported-operating-systems) then the extension will fail to install and you will see this message that we are waiting for data to arrive. 

If the VM has been running for 30+ minutes, has a supported operating system and you still see this message it often means that one or more of the extensions that get installed by Azure Monitor for VMs  have failed to install correctly. 

You can look on the Extension page for your resource to verify that the two extensions installed correctly.  
If you do not see the two extensions for your OS in the list of installed extensions, then they [need to be installed](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-enable-single-vm).  If the status does not appear as **Provisioning succeeded** then the extension should be removed and reinstalled

