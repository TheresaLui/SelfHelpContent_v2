<properties
	pageTitle="Azure-SSIS IR join vNet Issues"
	description="Troubleshooting Azure-SSIS IR Management - IR join vNet Issues"
	service="microsoft.datafactory"
	resource="factories"
	authors="chinadragon0515"
	ms.author="dashe"
	articleId="datafactory-newtree-ssis-ir-management-vnet.md"
	displayOrder="11"
	selfHelpType="generic"
	supportTopicIds="32680896"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Azure-SSIS IR join vNet Issues

The ADF Portal can be used to check the result of Azure SSIS IR start and there is detail error message shows on the ADF portal. The start result can also be retrieved via Azure powershell command.

## **Recommended Steps**

* Get the error code in the error message and then search the [troubleshoot document](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot) of the error code and find the detail cause and solution

## Common errors, causes, and solutions

When you join SSIS IR to Azure Virtual Network, SSIS IR uses the virtual network that's under the user subscription. For more information, see [Join an Azure-SSIS Integration Runtime to a virtual network](https://docs.microsoft.com/azure/data-factory/join-azure-ssis-integration-runtime-virtual-network).

When there's a Virtual Network-related issue, you'll see one of the following errors.

### **InvalidVnetConfiguration**

This error can occur for a variety of reasons. To troubleshoot it, see the [Forbidden](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot#forbidden), [InvalidPropertyValue](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot#invalidpropertyvalue), and [MisconfiguredDnsServerOrNsgSettings](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot#misconfigureddnsserverornsgsettings) sections.

  ### **Forbidden**

  This kind of error might resemble this: "SubnetId is not enabled for current account. Microsoft.Batch resource provider is not registered under the same subscription of VNet."

  These details mean that Azure Batch can't access your virtual network. Register the Microsoft.Batch resource provider under the same subscription as Virtual Network.

  ### **InvalidPropertyValue**

  This kind of error might resemble one of the following:

  - "Either the specified VNet does not exist, or the Batch service does not have access to it."
  - "The specified subnet xxx does not exist."

  These errors mean the virtual network doesn't exist, the Azure Batch service can't access it, or the subnet provided doesn't exist. Make sure the virtual network and subnet exist and that Azure Batch can access them.

  ### **MisconfiguredDnsServerOrNsgSettings**

  This kind of error message can look like this: "Failed to provision Integration Runtime in VNet. If the DNS server or NSG settings are configured, make sure the DNS server is accessible and NSG is configured properly."

  In this situation, you probably have a customized configuration of DNS server or NSG settings, which prevents the Azure server name required by SSIS IR from being resolved or accessed. For more information, see [SSIS IR Virtual Network configuration](https://docs.microsoft.com/azure/data-factory/join-azure-ssis-integration-runtime-virtual-network). If you’re still having problems, contact the Azure Data Factory support team.

### **VNetResourceGroupLockedDuringUpgrade**

SSIS IR will be automatically updated on a regular basis. A new Azure Batch pool is created during upgrade and the old Azure Batch pool is deleted. Also, Virtual Network-related resources for the old pool are deleted, and the new Virtual Network-related resources are created under your subscription. This error means that deleting Virtual Network-related resources for the old pool failed because of a delete lock at the subscription or resource group level. Because the customer controls and sets the delete lock, they must remove the delete lock in this situation.

### **VNetResourceGroupLockedDuringStart**

If SSIS IR provisioning fails, all the resources that were created are deleted. However, if there's a resource delete lock at the subscription or resource group level, Virtual Network resources are not deleted as expected. To fix this error, remove the delete lock and restart the IR.

### **VNetResourceGroupLockedDuringStop**

When you stop SSIS IR, all the resources related to Virtual Network are deleted. But deletion can fail if there's a resource delete lock at the subscription or resource group level. Here, too, the customer controls and sets the delete lock. Therefore, they must remove the delete lock and then stop SSIS IR again.

### **NodeUnavailable**

This error occurs when IR is running, and it means that IR has become unhealthy. This error is always caused by a change in the DNS server or NSG configuration that blocks SSIS IR from connecting to a necessary service. Because configuration of DNS server and NSG is controlled by the customer, the customer must fix the blocking issues on their end. For more information, see [SSIS IR Virtual Network configuration](https://docs.microsoft.com/azure/data-factory/join-azure-ssis-integration-runtime-virtual-network). If you’re still having problems, contact the Azure Data Factory support team.

## **Recommended Documents**

* [Join an Azure-SSIS integration runtime to a virtual network](https://docs.microsoft.com/azure/data-factory/join-azure-ssis-integration-runtime-virtual-network)
