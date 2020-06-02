<properties
    pageTitle="Azure Arc for Servers - Cannot install agent (Linux)"
    description="Azure Arc for Servers - Cannot install agent (Linux)"
    service="microsoft.hybridcompute"
    resource="hybridcompute"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32689153"
    resourceTags=""
    productPesIds="16872"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="ac3a1409-1fec-41f8-bcb1-443a43f9afde"
    ownershipId="Compute_HybridResourceProvider"
/>

# Installing the Azure Arc for Servers Agent

This article will help with issues installing the Azure Arc for Servers Agent on Windows.

## **Recommended Steps**

Please add '--verbose' to the onboarding command being executed and then collect the log files under '/var/opt/azcmagent/log'.

### **Prerequisites for Azure Arc for Servers**

* Most issues are caused by network configuration. Check the [Networking Configuration](https://docs.microsoft.com/azure/azure-arc/servers/overview#networking-configuration) document.

### **The subscription is not registered to use namespace Microsoft.HybridCompute**

* If you receive this message, follow the steps at [Register Azure Service Providers](https://docs.microsoft.com/azure/azure-arc/servers/overview#register-azure-resource-providers)