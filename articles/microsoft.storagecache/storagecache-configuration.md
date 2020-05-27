<properties
    pageTitle="Azure HPC Cache Post-Installation Configuration"
    description="Azure HPC Cache Post-Installation Configuration."
    infoBubbleText="Azure HPC Cache Post Installation Configuration."
    authors="cfriedel"
    ms.author="clfriede"
    displayOrder="1"
    articleId="storagecache-configuration"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32674484"
    resourceTags=""
    productPesIds="16790"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="StorageMediaEdge_HPCCache"
/>

# Azure HPC Cache Configuration

We have created this self-help article to assist with the post-installation configuration settings of the Azure HPC Cache.  If you need assistance with the installation or initial configuration of the Azure HPC Cache, please go to the *Get Started* portion of the [Azure HPC Cache Documentation](https://docs.microsoft.com/azure/hpc-cache/).

## **Recommended Steps**

### **Storage Targets**

1. If you should need to add a new storage target to your Azure HPC Cache namespace, you can do this by following the [Add Storage Targets](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-add-storage) page.

2. If you should need to modify or remove a storage target in your Azure HPC Cache namespace, you can do this by following the instructions on the [Edit Storage Targets](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-edit-storage) page.

### **Optional Configuration**

To change the optional configuration values of an Azure HPC Cache, please go to the Azure HPC Cache resource in the Azure Portal, then choose Configuration under the Settings heading on the Left-hand menu.  Once on the configuration page,  you can then change the following optional settings.

1. **MTU Size** - This setting will let you change the Maximum Transmission Unit (MTU) Size for packets on the Azure HPC Cache.  The default value of 1500 bytes should be acceptable for most networks, but there may be times you need to change it for VPNs that require smaller packet sizes.  If you should need to change this setting, please read [Adjust MTU Value](https://docs.microsoft.com/azure/hpc-cache/configuration#adjust-mtu-value).

2. **Root Squashing** - This setting will allow you to enable or disable root squashing for clients of the Azure HPC Cache.  Root squashing prevents the root user of a client from creating or modifying files and attributes on the HPC cache by reassigning the root UID of NFS calls to the UID of nobody.  By default, on caches created after April 2020, this setting will be enabled.  For caches created before this date, it may be disabled. If you wish to change the root squashing behavior of you Azure HPC Cache, please read [Configure Root Squash](https://docs.microsoft.com/azure/hpc-cache/configuration#configure-root-squash)

## **Recommended Documents**

* [Azure HPC Cache Documentation](https://docs.microsoft.com/azure/hpc-cache/)
* [Add Storage Targets](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-add-storage)
* [Edit Storage Targets](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-edit-storage)
* [Configure Additional Azure HPC Cache Settings](https://docs.microsoft.com/azure/hpc-cache/configuration)
* [Adjust MTU Size](https://docs.microsoft.com/azure/hpc-cache/configuration#adjust-mtu-value)
* [Configure Root Squash](https://docs.microsoft.com/azure/hpc-cache/configuration#configure-root-squash)
