<properties
	pageTitle="I tried to luanch a blade or section and received an "Access denied - You do not have access" message."
	description="I tried to luanch a blade or section and received an "Access denied - You do not have access" message."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="intuneroles_selfhelp"
	productPesIds=""
	cloudEnvironments="public"
/>

# I tried to luanch a blade or section and received an "Access denied - You do not have access" message.

## **Recommended steps**

* Ensure you have an Intune or EMS license assigned to the administrator's user account if they are a member of an Intune Custom Role.  You can assign licenses in the [Azure Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 Admin Center](https://portal.office.com/adminportal/home#/homepage).  Review the user licensing documentation for the [Azure Portal here](https://docs.microsoft.com/azure/active-directory/license-users-groups) or [here for the Office 365 Admin Center](https://docs.microsoft.com/intune/licenses-assign).

* Confirm the user does not have a Configuration Manager license assigned to them.

* Verify that you have been assigned the appropriate role-based administration control (RBAC) permissions in the Intune roles blade.

* Verify that your user account is not a member of a distribution group. Intune in the Azure portal only supports user accounts that belong to Azure Active security groups.  Review your groups in the Intune Groups blade or Azure Active Directory blade.



