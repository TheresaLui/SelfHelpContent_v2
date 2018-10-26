<properties
	pageTitle="Cannot activate role due to resource lock"
	description="When attempting to activate an Azure resource role you recieve an error resource locked"
	service="microsoft.aad"
	resource="Microsoft_Azure_PIM"
	authors="IdentityMy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32462545"
	resourceTags=""
	productPesIds="16577"
	cloudEnvironments="public"
/>

# Unable to activate roles due to Azure resource locks

Your Azure resources may be protected from accidental deletion with a policy that prohibits users from performing the delete action. If a policy is applied to a resource that prevents delete, it also prevents deleteion of role assignments in that resource. Privileged Identity Management is designed to provide zero-standing admin access and with delete locks enabled PIM is unable to remove role assignments at the end of the activation period. Since PIM is unable to funtion properly when a resource lock is applied, PIM prohibits users from activating roles until the delete lock is removed from the resource.

## **Recommended steps**


1. Remove the lock to continue using PIM. Use the following document to remove the resource lock and continue using PIM. [Remove Azure resource locks](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-lock-resources).


2. Make the user permanent or use a break-glass account. In the event you want to keep the resource lock, you should change your assignment to permanent or use a break-glass account until the resource lock is removed.  


## **Recommended documents**
* [Troubleshooting Elevated Permissions with Azure AD Privileged Identity Management](https://social.technet.microsoft.com/wiki/contents/articles/37568.troubleshooting-elevated-permissions-with-azure-ad-privileged-identity-management.aspx)<br>
* [Administrator roles in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
