<properties
	pageTitle="Problems configuring my resource to have a managed identity"
	description="Problems configuring my resource to have a managed identity"
	infoBubbleText="An issue was found with enabling managed identity on my resource"
	service="microsoft.azureactivedirectory"
	resource="userassignedidentities"
	authors="janelmsft"
	ms.author="janelg"
	displayOrder="3"
	articleId="8176e96a-f4d7-4bd1-bc0e-74ce4ce62819"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32690730"
	resourceTags=""
	productPesIds="16985"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureIdentity_Managed Identities"
/>

# Problems configuring my resource to have a managed identity

For issues related to configuring managed identity on a resource:

## **Recommended Steps**

- To enable system-assigned managed identity, you need write permissions over the resource. For example, for virtual machines you need Microsoft.Compute/virtualMachines/write. This action is included in resource specific built-in roles like Virtual Machine Contributor.
- To add a user-assigned managed identity to a resource, you need both write permissions over the resource and Managed Identity Operator permissions over the managed identity

## **Recommended Documents**

* [How to configure a user-assigned managed identity on a virtual machine](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vm#user-assigned-managed-identity)
* [How to configure a user-assigned managed identity on a virtual machine scale set](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vmss#user-assigned-managed-identity)
