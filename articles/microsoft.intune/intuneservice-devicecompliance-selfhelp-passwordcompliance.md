<properties
	pageTitle="Users with Windows devices are not being prompted for password compliance."
	description="Users with Windows devices are not being prompted for password compliance."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="devicecompliance_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5b47d6e1-f4f2-4dbe-9296-e804135c33fd"
	ownershipId="IntuneCxP_Intune"
/>

# Users with Windows devices are not being prompted for password compliance.

## **Recommended steps**

Password compliance policies only apply to local accounts. Azure Active Directory (Azure AD) users are subject to Azure AD password requirements and are not evaluated for conditional access.

For local accounts, this behavior is expected. The new password compliance rules will be enforced the next time the user signs out or signs in, or when they press **Ctrl-Alt-Del** and change their password. 
