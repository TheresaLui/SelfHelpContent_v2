<properties
	pageTitle="I don't see my Mac device under Intune in the Azure portal. It is, however, showing under Azure Active Directory."
	description="I don't see my Mac device under Intune in the Azure portal. It is, however, showing under Azure Active Directory."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="devicecompliance_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a6a71190-794b-4db1-ad94-462ac994068c"
	ownershipId="IntuneCxP_Intune"
/>

# I don't see my Mac device under Intune in the Azure portal. It is, however, showing under Azure Active Directory.

## **Recommended steps**

Complete the following steps to make sure Jamf is integrated with Intune.

1. Go to the Jamf self-service portal and launch the Company Portal app. For information about how to install and configure Jamf with Intune, see the following articles:

   * [Microsoft Intune and Jamf Pro: Better Together to Manage and Secure Macs](https://cloudblogs.microsoft.com/enterprisemobility/2017/12/14/microsoft-intune-and-jamf-pro-better-together-to-manage-and-secure-macs/)
   * [Integrate Jamf Pro with Intune for compliance](https://docs.microsoft.com/intune/conditional-access-integrate-jamf)

2. Tell the device owner to go to the Jamf self-service portal and re-run the device registration policy.  The Mac OS should now appear under the Intune device list in the Azure portal as well as in Azure AD.
