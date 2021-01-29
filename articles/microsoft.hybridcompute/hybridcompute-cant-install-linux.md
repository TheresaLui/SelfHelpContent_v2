<properties
  pagetitle="Azure Arc for Servers General Troubleshooting&#xD;"
  service="microsoft.hybridcompute"
  resource="machines"
  ms.author="t-juwa"
  selfhelptype="Generic"
  supporttopicids="32689165,32689166,32689162"
  resourcetags=""
  productpesids="16872"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="ac3a1409-1fec-41f8-bcb1-443a43f9afde"
  ownershipid="Compute_HybridResourceProvider" />
# Azure Arc for Servers General Troubleshooting

This article will help with issues regarding Arc for Servers Agent on Windows.

## **Recommended Steps**

Please add `--verbose` to the onboarding command being executed and then collect the log files under '%programdata%\AzureConnectedMachineAgent\Log' for Windows or '/var/opt/azcmagent/log' for Linux.

### **Prerequisites for Azure Arc for Servers**

* Most issues are caused by network configuration. Check the [Networking configuration](https://docs.microsoft.com/azure/azure-arc/servers/overview#networking-configuration) document.

### **The subscription is not registered to use namespace Microsoft.HybridCompute**

* If you receive this message, follow the steps at [Register Azure Service Providers](https://docs.microsoft.com/azure/azure-arc/servers/overview#register-azure-resource-providers)

### **Agent connection issues**

* [Agent connection issues to service](https://docs.microsoft.com/azure/azure-arc/servers/troubleshoot-agent-onboard#agent-connection-issues-to-service) lists some of the known errors and suggestions on how to troubleshoot and resolve them
