<properties
	pageTitle="Unable to manage role in a Microsoft Online Services portal after being assigned or activated"
	description="A user who has recently been assigned to a role or activated their role is not able to manage in some Microsoft Online Services portals"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32462545"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Unable to manage role in a Microsoft Online Services portal after being assigned or activated

Once a user is visible in Azure AD, that user can be assigned to Azure AD roles such as Security Administrator, using the interfaces of the Azure portal, PowerShell or Graph API.  Immediately after role assignment, the user themselves is able to manage Azure AD through those interfaces using that role. However, there may be a delay before the user is able to manage in other Microsoft Online Services using that role.  In other services, the user who has been recently assigned a role may not see an administrative portal or may receive "access denied" messages.

## **Recommended steps**


1. Verify the user's role assignments are correct in Azure AD.  The easiest way to do this is via PowerShell, using either the Microsoft Online Services [Get-MsolUserRole](https://docs.microsoft.com/powershell/msonline/v1/get-msoluserrole) cmdlet or Azure AD v2 PowerShell [Get-AzureADDirectoryRoleMember](https://docs.microsoft.com/powershell/azuread/v2/get-azureaddirectoryrolemember) cmdlet.  For example, this command response illustrates that a user currently has two administrative role assignments in Azure AD.

```
PS> Get-MsolUserRole -UserPrincipalName user@cexample.onmicrosoft.com

ObjectId                               Name                             Description
--------                               ----                             -----------
62e90394-69f5-4237-9190-012177145e10   Company Administrator            Company Administrator role has full access ...
e8611ab8-c189-46e8-94e1-60213ab1f814   Privileged Role Administrator    Privileged Role Administrator has access to...
```
2. If the user is going to be managing Azure AD in the Azure portal, have them refresh their browser view of the web page. If the user is going to be managing in an Office 365 portal, then after a short delay, have the user re-open the portal web page.  


## **Recommended documents**
* [Troubleshooting Elevated Permissions with Azure AD Privileged Identity Management](https://social.technet.microsoft.com/wiki/contents/articles/37568.troubleshooting-elevated-permissions-with-azure-ad-privileged-identity-management.aspx)<br>
* [Administrator roles in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
