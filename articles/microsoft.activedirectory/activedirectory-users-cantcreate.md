<properties 
    pageTitle="I can't create a new user in my Azure AD"
    description="I can't create a new user in my Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authorAlias="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32045780"
    productPesIds="14785,16578"
    cloudEnvironments="public"
    />

# I can't create a new user in my Azure AD directory

## **Recommended steps**

1. Ensure that you are authorized to create a new standard user. Only the Global Administrator or User Account Administrator role in Azure AD can create a new standard user. If you are not in one of these roles, ask an administrator create the new user for you or add you to one of these roles.<br>  
2. Ensure that the user name is in a domain that is verified in your Azure AD. If you do not have any verified custom domain names in your Azure AD, you can add a with a user name in your initial domain name, which ends with *.onmicrosoft.com.<br>
3. Ensure that the user name is in a domain that is not federated to Azure AD from your on-premises AD. Users cannot be added in the cloud with domain names that are federated with your Azure AD.<br>
4. Ensure that no other user or contact already has the user name that you want to assign to the new user. User names must be unique across Azure AD.<br>

### **Recommended tools**

* See the [Azure AD roles and administrators](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RolesAndAdministrators) for your Azure AD.<br>
* See the [domain names](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains) for your Azure AD.

## **Recommended documents**

* [Use the Azure portal to create a new user in your Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-users-create-azure-portal)<br>
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)<br>
* [Use Azure AD PowerShell to create a new user](https://docs.microsoft.com/powershell/azuread/v2/new-azureaduser)