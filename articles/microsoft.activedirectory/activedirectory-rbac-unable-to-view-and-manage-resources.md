<properties
    pageTitle="I can’t add or manage resources in my directory"
    description="I can’t add or manage resources in my directory"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder="2523"
    selfHelpType="resource"
    resourceTags="Azure_RBAC"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="8bc25c45-f8e0-4630-bdc1-123da5078d4e"
	ownershipId="AzureIdentity_User"
/>

# Unable to view and manage Azure resources

## **Recommended steps**

**Verify whether you are signing into the account that is associated with the subscription.** 
If you have both Azure AD and Microsoft accounts, you might be signing in with a personal account instead of a work or school account. If this is the case, sign into the desired account and consider [renaming your personal account](https://support.microsoft.com/help/11545/microsoft-account-rename-your-personal-account).

**Verify whether you have the appropriate permissions to view the subscription.**

1.	Sign in to [the Azure portal](https://portal.azure.com) with an account that is a global administrator for the directory.
2.	Select **Users and groups**, and then either **All users** or **All groups**.
3.	Search for the user and open the user blade.
4.	Select **Azure resources** on the user blade. All the access assignments for that user appear. 
5.	Confirm that you have sufficient permissions to view the subscription. If you do not, contact your IT admin to receive permissions. 

**Verify whether you are viewing the correct directory in the Azure portal.**

You might have selected the wrong directory in the Azure portal.
 
1.	To confirm, select your user profile at the top right hand corner in the Azure portal.
2.	Verify whether the directory that you are in is the right directory. If not, switch to the directory you want. 

**Verify whether you are filtering out some subscriptions in the resource blade (All Resources or Resource Groups) in the Azure portal.**

## **Recommended documents**
* [Managing access assignments by user](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-assignments)
* [Managing access assignments by resource](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure)
* [Built-in roles for Azure RBAC](https://docs.microsoft.com/azure/active-directory/role-based-access-built-in-roles)
