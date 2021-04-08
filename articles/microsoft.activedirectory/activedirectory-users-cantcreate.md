<properties
  pagetitle="I can't create a new user in my Azure AD directory"
  service="microsoft.aad"
  resource="microsoft_aad_iam"
  ms.author="jupetter"
  selfhelptype="Generic"
  supporttopicids="32045780"
  resourcetags=""
  productpesids="16578"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="e8088803-9c36-4f17-9ff5-3e8ba3e20813"
  ownershipid="AzureIdentity_DirectoryObjectManagement" />
# I can't create a new user in my Azure AD directory

## **Recommended Steps**

1. Ensure that you are authorized to create a new standard user. Only the Global administrator or User administrator role in Azure Active Directory (AD) can create a new standard user. If you're not in one of these roles, ask an administrator to add you to one of these roles or to create the new user account for you.<br>  
2. Ensure that the user name is in a domain that is verified in your Azure AD. If you do not have any verified custom domain names in your Azure AD, you can use your Azure AD initial domain, which ends with *.onmicrosoft.com.<br>
3. Ensure that the user name is in a domain that is not federated to Azure AD from your on-premises AD. Users cannot be added in the cloud with domain names that are federated from on-premises.<br>
4. Ensure that no other user or contact already has the user name that you want to assign to the new user. User names must be unique across Azure AD.<br>
5. See [Azure AD roles and administrators](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RolesAndAdministrators) for your Azure AD.<br>
6. See the [domain names](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains) for your Azure AD.<br>
7. Review [Audit logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Audit) to see more detailed information about a recently created or deleted user like who performed the action and when. 

## **Recommended Documents**

* [Use the Azure portal to create a new user in your Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-users-create-azure-portal)<br>
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)<br>
* [Use Azure AD PowerShell to create a new user](https://docs.microsoft.com/powershell/module/azuread/new-azureaduser?view=azureadps-2.0) <br>
* [Self-service sign up for Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-self-service-signup)
