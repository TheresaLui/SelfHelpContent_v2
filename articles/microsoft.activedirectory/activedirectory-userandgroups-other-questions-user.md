<properties 
    pageTitle="Other questions regarding user and group management"
    description="Other questions regarding user and group management"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32565604"
    productPesIds="14785"
    cloudEnvironments="public"
 />
 
# Other questions regarding user and group management

## **Recommended steps**
1. Ensure you are assigned to a directory role that is authorized to perform the operation. Most operations on users and groups can be performed only by global administrators and user administrators. Permissions to an Azure subscription do not convey permissions to manage the Azure AD that is associated with the subscription. Learn more about [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles).
2. If you are attempting to update or delete a user or a group, ensure that the user or group is not synced from your on-premises Active Directory. Most changes on synced users and groups must be made in your on-premises directory. Those changes will then be synced to your Azure AD.
3. If you are defining an advanced dynamic membership rule for a group, ensure that your rule uses the supported syntax. Learn more about [dynamic membership rules](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).

## **Recommended documents**

* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
* [How your Azure subscription is related to your Azure AD tenant](https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory#how-an-azure-subscription-is-related-to-azure-ad)
* [Use Azure AD PowerShell to manage users](https://docs.microsoft.com/powershell/azuread/v2/azureactivedirectory#users)
* [Use Azure AD PowerShell to manage groups](https://docs.microsoft.com/powershell/azuread/v2/azureactivedirectory#groups)

