<properties 
    pageTitle="Problem deleting a user or restoring a deleted user"
    description="Problem deleting a user or restoring a deleted user"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT" 
    selfHelpType="generic"
    supportTopicIds="32586793"
    productPesIds="14785"
    cloudEnvironments="public"
    />


# I can't delete a user in my directory, or restore a deleted user 

## **Recommended steps**

1.	Ensure that you are authorized to delete or restore a user. Only a global administrator or user administrator of Azure AD can perform these tasks. If you are not in one of these roles, you must ask an administrator to update the user properties for you, or to add you to one of these roles. [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)

## **Recommended documents**

* [Use PowerShell to delete a user](https://docs.microsoft.com/powershell/azuread/v2/set-azureaduser)<br>
* [Use PowerShell to restore a deleted user](https://docs.microsoft.com/powershell/module/msonline/restore-msoluser?view=azureadps-1.0)<br>
* [Use PowerShell to permanently delete a user by removing the user from the recycle bin](https://docs.microsoft.com/powershell/module/MSOnline/Remove-MsolUser?view=azureadps-1.0#optional-parameters)<br>
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) 