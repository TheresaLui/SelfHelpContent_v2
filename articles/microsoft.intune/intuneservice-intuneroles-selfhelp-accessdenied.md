<properties
	pageTitle="I tried to access a section in the Intune portal and received an Access denied message."
	description="I tried to access a section in the Intune portal and received an Access denied message."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="intuneroles_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a772737e-37c2-493c-8da6-e00d9c48a62b"
	ownershipId="IntuneCxP_Intune"
/>

# I tried to access a section in the Intune portal and received an "Access denied" message.

## **Recommended steps**

* If you are a member of an Intune custom role, ensure that an Intune or Enterprise Mobility Suite (EMS) license is assigned to your account.  Assign licenses in the [Azure portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 admin center.](https://portal.office.com/adminportal/home#/homepage)  Find out more about user licensing from the [Azure Active Directory documentation](https://docs.microsoft.com/azure/active-directory/license-users-groups) and [ Office 365 admin center documentation.](https://docs.microsoft.com/intune/licenses-assign)

* If you are using Configuration Manager to manage devices verify you are not part of the Intune user collection for Configuration Manager MDM.  Find out more about the Configuration Manager user collection from the [SCCM MDM documentation.](https://docs.microsoft.com/sccm/mdm/deploy-use/configure-intune-subscription#to-create-the-microsoft-intune-subscription)

* Verify that you have been assigned the appropriate role-based administration control (RBAC) permissions in the Intune roles blade.

* Verify the group used is not a distribution list. Intune in the Azure portal only supports user accounts that belong to Azure Active Directory security groups.  Review your groups in the Azure portal > **Intune** > **Groups** or in Azure portal > **Azure Active Directory**.
