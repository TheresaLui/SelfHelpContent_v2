<properties
	pageTitle="Synchronizing AD to Azure AD/Password synchronization"
	description="Synchronizing AD to Azure AD/Password synchronization"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cychua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32142240"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Synchronizing AD to Azure AD/Password synchronization

## **Recommended steps**

1. Determine whether the issue is affecting all users or only specific user(s).

2. If the issue is affecting all users:
    1. Make sure the Password Synchronization feature is correctly configured on your Azure AD Connect server and your server is not in staging mode.
    2. Look in the Windows event log for errors which may indicate connectivity issue.    
    3. Make sure the user account used by Azure AD Connect to synchronize changes from on-premises AD is granted following permissions to your on-premises AD:
        * Replicate Directory Changes
        * Replicate Directory Changes All
		
3. If the issue is affecting only specific user(s):

    1. Make sure the user object is syncing correctly to Azure AD.
    2. Look in the password sync log for errors related to this user object which may indicate the issue.
    3. Make sure the on-premises AD user object is not configured with the option "User must change password at next logon". Azure AD Connect does not synchronize temporary passwords to Azure AD.


## **Recommended documents**
[Implement password synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization)
<br>
[Troubleshoot password synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization)
<br>
