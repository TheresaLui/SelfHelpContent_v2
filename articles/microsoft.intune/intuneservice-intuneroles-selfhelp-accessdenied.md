<properties
	pageTitle="I tried to launch a blade or section and received an Access denied - You do not have access message."
	description="I tried to launch a blade or section and received an Access denied - You do not have access message."
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

# I tried to launch a blade or section and received an "Access denied - You do not have access" message

## **Recommended steps**

* If you are a member of an Intune custom role, ensure that an Intune or Enterprise Mobility Suite (EMS) license is assigned to your account.  Assign licenses in the [Azure portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 admin center](https://portal.office.com/adminportal/home#/homepage).  Find out more about user licensing from the [Azure portal documentation](https://docs.microsoft.com/azure/active-directory/license-users-groups) or the [ Office 365 admin center documentation](https://docs.microsoft.com/intune/licenses-assign).

* If you are also using Configuration Manager ensure the user is not part of the user collection for Configuration Manager MDM. Find out  more about the Configuration Manager user collection from the [SCCM MDM documentation](https://docs.microsoft.com/sccm/mdm/deploy-use/configure-intune-subscription#to-create-the-microsoft-intune-subscription).

* Verify that you have been assigned the appropriate role-based administration control (RBAC) permissions in the Intune roles blade.

* Verify that your user account is not a member of a distribution group. Intune in the Azure portal only supports user accounts that belong to Azure Active Directory security groups.  Review your groups in the Intune groups blade or Azure Active Directory blade.



