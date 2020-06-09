<properties
    pageTitle="Azure Arc for Servers - Other issues"
    description="Azure Arc for Servers - Other issues"
    service="microsoft.hybridcompute"
    resource="hybridcompute"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="
32689165,
32689166,
32689155,
32689156,
32689163,
32689167,
32689164,
32689168,
32689160,
32689161,
32689162
"
    resourceTags=""
    productPesIds="16872"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="57ca1e41-f9db-450e-89b5-03b7b69b39c7"
    ownershipId="Compute_HybridResourceProvider"
/>

# Installing the Azure Arc for Servers Agent

This article will help with regarding Azure Arc for Servers Agent on Windows.

## **Recommended Steps**

Please add '--verbose' to the onboarding command being executed and then collect the log files under '%programdata%\AzureConnectedMachineAgent\Log' for Windows or '/var/opt/azcmagent/log' for Linux.

### **Prerequisites for Azure Arc for Servers**

* Most issues are caused by network configuration. Check the [Networking Configuration](https://docs.microsoft.com/azure/azure-arc/servers/overview#networking-configuration) document.

### **The subscription is not registered to use namespace Microsoft.HybridCompute**

* If you receive this message, follow the steps at [Register Azure Service Providers](https://docs.microsoft.com/azure/azure-arc/servers/overview#register-azure-resource-providers)