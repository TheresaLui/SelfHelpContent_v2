<properties 
    pageTitle="Other problems managing a user"
    description="Other problems managing a user"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32565604"
    productPesIds="14785"
    cloudEnvironments="public"
    />


# I can't update the properties of a user in my Azure AD tenant 

## **Recommended steps**

1.	Ensure that you are authorized to update user properties. Only a global administrator or user administrator of Azure AD can update user properties. If you are not in one of these roles, you must ask an administrator to update the user properties for you, or to add you to one of these roles. [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2.	Ensure that you are not updating a property that is synced from your on-premises AD. If the user is synced (that is, if Source = 'Windows Server AD'), then the only properties that can be managed in Azure AD are in the **Settings** and **Authentication** contact info sections. To change any other property, change it in your on premises directory. You czn see the updated property in the cloud after the next time sync runs.
3. If you are defining an advanced dynamic membership rule for a group, ensure that your rule uses the supported syntax. Learn more about [dynamic membership rules](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).

## **Recommended documents**

* [Use the Azure portal to change profile information for a user](https://docs.microsoft.com/azure/active-directory/active-directory-users-profile-azure-portal)<br>
* [Use PowerShell to update profile properties for a user](https://docs.microsoft.com/powershell/azuread/v2/set-azureaduser)<br>
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) 