<properties
	pageTitle="User assigned managed identity with Virtual Machines"
	description="I can't add a user-assigned managed identity to my VM/VMSS"
	infoBubbleText="An issue was found with a user assigned managed identity on VM/VMSS"
	service="microsoft.azureactivedirectory"
	resource="userassignedidentities"
	authors="arluca"
	ms.author="arluca"
	displayOrder="1"
	articleId="user-assigned managed identity integration with VM-VMSS"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32632153"
	resourceTags=""
	productPesIds="16575"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AppDevelopmentAndRegistration"
/>

# <-- I can't add a user-assigned managed identity to a Virtual Machine/Virtual Machine Scale Set -->

For issues related to adding a user-assigned managed identity to a Virtual Machine or Virtual Machine Scale Set:

## **Recommended Steps**

1. Verify you have the Managed Identity Operator role assignment on the user-assigned managed identity
2. Verify you have the Virtual Machine Contributor role assignment on the Virtual Machine

## **Recommended Documents**

* [How to configure a user-assigned managed identity on a virtual machine](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vm#user-assigned-managed-identity)
* [How to configure a user-assigned managed identity on a virtual machine scale set](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vmss#user-assigned-managed-identity)
