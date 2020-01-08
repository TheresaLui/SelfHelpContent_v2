<properties
	pageTitle="Problems configuring my resource to have a managed identity"
	description="Problems configuring my resource to have a managed identity"
	infoBubbleText="An issue was found with enabling managed identity on my resource"
	service="microsoft.azureactivedirectory"
	resource="userassignedidentities"
	authors="arluca"
	ms.author="arluca"
	displayOrder="1"
	articleId="8eda095f-de94-4896-a4a7-537c78b9f073"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32690730"
	resourceTags=""
	productPesIds="16985"
	cloudEnvironments="public, blackForest, fairfax, mooncake"
/>

# Problems configuring my resource to have a managed identity

For issues related to configuring managed identity on a resource:

## **Recommended Steps**

- To enable system-assigned managed identity, you need write permissions over the resource. 
For example, for virtual machines you need Microsoft.Compute/virtualMachines/write. This action is included in resource specific built-in roles like Virtual Machine Contributor.

- To add a user-assigned managed identity to a resource, you need both write permissions over the resource and Managed Identity Operator permissions over the managed identity. 

## **Recommended Documents**

* [How to configure a user-assigned managed identity on a virtual machine](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vm#user-assigned-managed-identity)
* [How to configure a user-assigned managed identity on a virtual machine scale set](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vmss#user-assigned-managed-identity)
