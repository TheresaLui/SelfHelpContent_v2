
<properties
	pageTitle="Why is there no MDM or Compliant status on my device?"
	description="Azure AD Devices self help - MDM and Compliant fields"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="spunukol"
	displayOrder="200"
	selfHelpType="resource"
	supportTopicIDs=""
	resourceTags="devices_overview"
	productPesIds=""
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="ba8d40d9-9b48-47a5-be9c-afb7ff2f8df7"
	ownershipId="AzureIdentity_User"
/>

# Why is there no MDM or Compliant status on my device?

## **Recommended steps**

1. If a device has been enrolled for device management, MDM (Mobile Device Management) is updated with the management owner. 
2. If a device is enrolled, the compliant status is updated by the management owner.
3. Device that Hybrid Azure AD joined and managed by SCCM will have a compliant status without a management owner.
4. The compliant status is marked as N/A in all other conditions not stated above.

## **Recommended documents**

* [Devices Introduction](https://docs.microsoft.com/azure/active-directory/device-management-introduction)
