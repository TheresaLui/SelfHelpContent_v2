<properties
  pagetitle="Common Permissions-Related Issues"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="pazand"
  selfhelptype="Generic"
  supporttopicids="32572359"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azuredevopspermissionsrelatedselfservicescenarios"
  ownershipid="Azure_DevOps_Services" />
# Common Permissions-Related Issues

## **Recommended Steps** 

**How do I find my admin?**

* [Find your administrator](https://docs.microsoft.com/azure/devops/organizations/security/lookup-organization-owner-admin?view=azure-devops&amp;tabs=preview-page)

**I added a user to my project. Why can't they see the project?**

* In order to view a [project](https://docs.microsoft.com/azure/devops/organizations/security/permissions?view=azure-devops&amp;tabs=preview-page#project-level-groups), users must have the ["view project level information" permission set to "allow"](https://docs.microsoft.com/azure/devops/organizations/security/set-project-collection-level-permissions?toc=%2Fazure%2Fdevops%2Fsecurity-access-billing%2Ftoc.json&amp;bc=%2Fazure%2Fdevops%2Fsecurity-access-billing%2Fbreadcrumb%2Ftoc.json&amp;view=azure-devops&amp;tabs=preview-page)

**I accidentally removed my permissions, and am unable to grant them again. What should I do?**

* The only way to resolve this scenario is to [find your project/org admin](https://docs.microsoft.com/azure/devops/organizations/security/lookup-organization-owner-admin?view=azure-devops&amp;tabs=preview-page) and ask them to grant the permission again

**How do I remove users from Azure DevOps?**

* [How to remove users from Azure DevOps](https://docs.microsoft.com/azure/devops/organizations/accounts/delete-organization-users?view=azure-devops&amp;tabs=preview-page)

**Why can't I create an organization?**

* Contact your administrator to determine if your organization is using [the Azure AD tenant policy to restrict new org creation](https://docs.microsoft.com/azure/devops/organizations/accounts/azure-ad-tenant-policy-restrict-org-creation?view=azure-devops)

**Why can't guest users search for AAD users?**

* By default, [Azure AD guests can't search the Azure AD in the manner required by Azure DevOps](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-azure-access?view=azure-devops#q-why-are-no-identities-found-when-i-try-to-add-users-from-azure-ad-to-my-azure-devops-organization)
