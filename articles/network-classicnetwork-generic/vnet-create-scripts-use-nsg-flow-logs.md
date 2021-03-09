<properties
    pageTitle="Azure Virtual Network - Create scripts and use NSG flow logs"
    description="Azure Virtual Network - Create scripts and use NSG flow logs"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781387"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e569aee9-37c8-4a05-9e83-40c985e143e8"
/>

# Azure Virtual Network - Create scripts and use NSG flow logs

## **Recommended Steps**

1. Use the sample script at [Collect details about all VMs in a subscription with PowerShell](https://docs.microsoft.com/azure/virtual-machines/scripts/virtual-machines-powershell-sample-collect-vm-details) to find all application security groups (ASGs) associated with virtual machines (VMs) in your subscription

2. If no traffic is being logged, your VMs may not be active or an App Gateway, firewall, or other device could be blocking traffic

3. Check that the storage account used for the Flow Logs is in the same region as the network security group (NSG). If you change or rotate the access keys to your storage account, NSG Flow Logs will stop working. To fix this issue, disable and re-enable NSG Flow Logs.

## **Recommended Documents**

- [Introduction to using flow logging for NSGs](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-overview)
- [Enabling NSG Flow Logs](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-overview#enabling-nsg-flow-logs)
- [Reading network flow logs](https://docs.microsoft.com/azure/network-watcher/network-watcher-read-nsg-flow-logs)
- [Using Traffic Analytics to analyze flow logs](https://docs.microsoft.com/azure/network-watcher/traffic-analytics)
