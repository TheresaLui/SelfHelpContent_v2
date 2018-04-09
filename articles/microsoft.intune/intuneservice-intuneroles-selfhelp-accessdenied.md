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

* If you are a member of an Intune custom role, ensure that an Intune or Enterprise Mobility Suite (EMS) license is assigned to your account.  Assign licenses in the [Azure portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 admin center](https://portal.office.com/adminportal/home#/homepage).  Find out more about user licensing from the [Azure Portal documentation](https://docs.microsoft.com/azure/active-directory/license-users-groups) or the [ Office 365 admin center documentation](https://docs.microsoft.com/intune/licenses-assign).

* Confirm the user does not have a Configuration Manager license assigned to them in the Configuration Manager console.

* Verify that you have been assigned the appropriate role-based administration control (RBAC) permissions in the Intune roles blade.

* Verify that your user account is not a member of a distribution group. Intune in the Azure portal only supports user accounts that belong to Azure Active security groups.  Review your groups in the Intune groups blade or Azure Active Directory blade.



