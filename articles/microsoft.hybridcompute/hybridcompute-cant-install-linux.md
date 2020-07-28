<properties
  pagetitle="Installing the Azure Arc for Servers Agent"
  service="microsoft.hybridcompute"
  resource="hybridcompute"
  ms.author="t-juwa"
  selfhelptype="Generic"
  supporttopicids="32689163,32689164,32689153,32689154,32689155,32689156,32689165,32742674,32689160,32689161,32689166,32742675,32689162,32689167,32689168,32742676"
  resourcetags=""
  productpesids="16872"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="ac3a1409-1fec-41f8-bcb1-443a43f9afde"
  ownershipid="Compute_HybridResourceProvider" />
# Installing the Azure Arc for Servers Agent

This article will help with issues installing the Azure Arc for Servers Agent on Windows.

## **Recommended Steps**

Please add '--verbose' to the onboarding command being executed and then collect the log files under '/var/opt/azcmagent/log'.

### **Prerequisites for Azure Arc for Servers**

* Most issues are caused by network configuration. Check the [Networking Configuration](https://docs.microsoft.com/azure/azure-arc/servers/overview#networking-configuration) document.

### **The subscription is not registered to use namespace Microsoft.HybridCompute**

* If you receive this message, follow the steps at [Register Azure Service Providers](https://docs.microsoft.com/azure/azure-arc/servers/overview#register-azure-resource-providers)