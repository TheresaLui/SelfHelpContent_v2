<properties
	pageTitle="Set up Intune - Setup administrators and manage roles"
	description="Set up Intune - Setup administrators and manage roles"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599674"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="86df0e1a-c14b-48a6-a7ce-a1a090cd0ca7"
	ownershipId="IntuneCxP_Intune"
/>

# Set up Intune - Setup administrators and manage roles

Let's take a look at a couple few common issues using Intune Roles and how to resolve them:

**I tried to access a section in the Intune portal and received an "Access denied" message.**

* If you are a member of an Intune custom role, ensure that an Intune or Enterprise Mobility Suite (EMS) license is assigned to your account.  Assign licenses in the [Azure portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 admin center.](https://portal.office.com/adminportal/home#/homepage)  Find out more about user licensing from the [Azure Active Directory documentation](https://docs.microsoft.com/azure/active-directory/license-users-groups) and [ Office 365 admin center documentation.](https://docs.microsoft.com/intune/licenses-assign)

* If you are using Configuration Manager to manage devices verify you are not part of the Intune user collection for Configuration Manager MDM.  Find out more about the Configuration Manager user collection from the [SCCM MDM documentation.](https://docs.microsoft.com/sccm/mdm/deploy-use/configure-intune-subscription#to-create-the-microsoft-intune-subscription)

* Verify that you have been assigned the appropriate role-based administration control (RBAC) permissions in the Intune roles blade.

* Verify the group used is not a distribution list. Intune in the Azure portal only supports user accounts that belong to Azure Active Directory security groups.  Review your groups in the Azure portal > **Intune** > **Groups** or in Azure portal > **Azure Active Directory**.

**One of my users seems to have too many permissions for the role I've assigned them in Intune.**

Advise the user to go to **Intune** > **Intune roles** > **My permissions** > **Export**. If needed, you can adjust their permissions in Intune roles. 

**I added a scope group to a role, but users in that role still see other users or devices.**<br>

Scope groups do not filter out users or devices.  Rather scope groups:

* Limit who users can assign policies or applications to
* Allow only specific users to run remote tasks on devices

If a security group is not within your scope group, you will not be able to assign polices or applications to the group. For more information about scope groups see the [Intune documentation.](https://docs.microsoft.com/intune/role-based-access-control)

**I added a user to an Intune role but they still have full access to the Intune admin console.**<br>

Verify that the user is not assigned to any of the following roles in the Azure portal:

* Global administrator
* Intune service administrator
* SharePoint administrator

Verify that the user is not assigned to the following role in the Intune classic portal:

* Service administrator

Users in these roles have full access to Intune in the Azure portal. To check the role of a user in the Azure portal go to **Intune** > **Users**. To check the role of a user in the classic portal go to **Admin** > **Service Administrators**.<br>

Below is a list of additional resources and documentation that may also assist in resolving your issue.  Please review before opening a support case.

## **Recommended documents**
[Role-based administration control with Microsoft Intune](https://docs.microsoft.com/intune/role-based-access-control)<br>
[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>