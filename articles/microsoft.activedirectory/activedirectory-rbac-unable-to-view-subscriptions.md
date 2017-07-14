<properties 
    pageTitle="I can’t add or manage resources in my directory"
    description="I can’t add or manage resources in my directory"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jeffsta-MSFT"
    displayOrder="2524"
    selfHelpType="resource"
    resourceTags="directory_overview"
    cloudEnvironments="public"
    />

# Unable to view subscriptions in the Azure portal

## **Recommended steps**

**Verify whether you are signing in to the account that is associated with the subscription.** 
If you have both Azure AD and Microsoft accounts, you might be signing in with a personal account instead of a work or school account. If this is the case, sign into the desired account and consider renaming your personal multi-factor authentication here.

**Verify whether you have the appropriate permissions to view the subscription.**
1.	Sign in to Azure AD with an account that is a global administrator for the directory.
2.	Select **Users and groups**, and then either **All users** or **All groups**.
3.	Search for the user and open the user blade.
4.	Select **Azure resources** on the user blade. All the access assignments for that user appear. 
5.	Confirm that you have sufficient permissions to view the subscription. If you do not, contact your IT admin to receive permissions. 

**Verify whether you are viewing the correct directory in the Azure Portal.**
1.	You might have selected the wrong directory in the Azure portal. 
2.	To confirm, select your user profile at the top right hand corner in the Azure portal.
3.	Verify whether the directory that you are in is the right directory. If not, switch to the directory you want. 

## **Recommended documents**
* [Managing access assignments by user](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-assignments)
* [Managing access assignments by resource](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure)
* [Built-in roles for Azure RBAC](https://docs.microsoft.com/azure/active-directory/role-based-access-built-in-roles)
