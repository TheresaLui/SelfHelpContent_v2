<properties
	pageTitle="Problem with assigning group to an Azure AD role"
	description="Problem with assigning group to an Azure AD role"
	infoBubbleText=""
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	ms.author="absinh"
	displayOrder=""
	articleId="b8cc147a-11ba-4f16-8f0e-c41f466abf65"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32736802"
	resourceTags=""
	productPesIds="16578"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem with assigning group to an Azure AD role

Most users are able to resolve their issue related to assigning groups to Azure AD roles using the steps below.

## **Recommended Steps**

### **Assign a group to Azure AD role**

* To assign an Azure AD group (whose source of authority is in Azure AD) to an Azure AD role, start with creating a new group
* Sign in to the Azure AD admin center with Privileged Role Administrator or Global Administrator permissions in the Azure AD organization
* Select Azure Active Directory > Groups > All groups > New group
* Switch on the toggle "Azure AD roles can be assigned to the group" and create the group
* You can assign role the role to the group during creation or you can go to "Assigned roles" tab of the group later on and add role assignment

### **Manage membership of a group that is assigned to Azure AD role**

To prevent elevation of privilege, by default only Privileged Role Administrator and Global Administrator can modify the membership of a group that is assigned to role. They can, however, choose to assign an owner on such group and delegate this task.

## **Recommended Documents**

* [Use cloud groups to manage role assignments in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/roles-groups-concept)
* [Troubleshooting roles assigned to cloud groups](https://docs.microsoft.com/azure/active-directory/users-groups-roles/roles-groups-faq-troubleshooting)
