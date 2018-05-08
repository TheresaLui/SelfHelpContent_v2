<properties
    pageTitle="Azure AD roles and permissions"
    description="Azure Active Directory case submission self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045782"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# Azure AD roles and permissions 
 
## **Recommended steps** 
1. Ensure you are assigned to a directory role that is authorized to manage roles in Azure AD. The roles authorized to manage roles for other users are Global Administrator and Privileged Identity Manager. Permissions to an Azure subscription do not convey permissions to manage the Azure AD tenant that is associated with the subscription. Learn more about [Azure AD administrative roles](https://docs.microsoft.com/azure/activedirectory/active-directory-assign-admin-roles-azure-portal).
2. Assign the role that corresponds to the permissions that the user needs in your Azure AD. To assign the role, navigate to the ‘directory role’ tab for the user. [Learn about the permissions of each Azure AD role](https://docs.microsoft.com/azure/activedirectory/active-directory-assign-admin-roles-azure-portal#administrator-permissions).
3. If you need to assign access to an Azure subscription, or a resource within a subscription such as a virtual machine, navigate to the Azure resource and assign access there. Azure AD role assignments do not convey access to manage Azure subscription resources. [Assign access to Azure resources in the Azure portal](https://docs.microsoft.com/azure/activedirectory/role-based-access-control-configure#add-access).

## **Recommended documents** 
 
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directoryassign-admin-roles)
* [How your Azure subscription is related to your Azure AD](https://docs.microsoft.com/azure/activedirectory/active-directory-how-subscriptions-associated-directory#how-an-azure-subscription-isrelated-to-azure-ad)
* [Use PowerShell to add a user to an Azure AD role](https://docs.microsoft.com/powershell/azuread/v2/add-azureaddirectoryrolemember)
* [Use PowerShell to manage access to Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-access-powershell) 