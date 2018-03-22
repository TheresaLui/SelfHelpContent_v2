<properties
	pageTitle="I receive an Access Denied error while trying to launch a blade or section of the Microsoft Intune UI"
	description="I receive an Access Denied error while trying to launch a blade or section of the Microsoft Intune UI"
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

# I receive an "access denied" error while trying to launch a blade or section

## **Recommended steps**

<<<<<<< HEAD
1. Ensure you have an Intune or EMS license assigned to the administrator's user account if they are a member of an Intune Custom Role.  You can assign licenses in the [Azure Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 Admin Center](https://portal.office.com/adminportal/home#/homepage).  Review the user licensing documentation for the [Azure Portal here](https://docs.microsoft.com/azure/active-directory/license-users-groups) or [here for the Office 365 Admin Center](https://docs.microsoft.com/intune/licenses-assign).
=======
1. Ensure you have an Intune or EMS license assigned to the administrator's user account if they are a member of an Intune custom role.  You can assign licenses in the [Azure Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 Admin Center](https://portal.office.com/adminportal/home#/homepage).  Review the user licensing documentation for the [azure portal here](https://docs.microsoft.com/azure/active-directory/license-users-groups) or [here for the office 365 admin center](https://docs.microsoft.com/intune/licenses-assign).
>>>>>>> parent of 5152255a... changes to case

2. Confirm the user does not have a Configuration Manager license assigned to them.

3. Verify correct RBAC permissions are assigned.

4. Verify the user who belongs to the group is not a distribution group, only security groups are allowed.



