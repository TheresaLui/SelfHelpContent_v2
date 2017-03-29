<properties 
    pageTitle="A user doesn't have licenses that they should have"
    description="A user doesn't have licenses that they should have"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1771"
    supportTopicIds=""
    selfHelpType="resource"
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
 />

# A user doesn't have licenses that they should have

The full information about user licenses and their status is available on the **Licenses** blade for that user. If you don't see the licenses that you expect, consider the following:

1. If you are using group-based licensing to assign licenses to your users, it is possible that the system could not assign the license. This information is shown on the **Licenses** tab for the user. See the article on [docs.microsoft.com](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-problem-resolution-azure-portal) about identifying and resolving license problems with group-based licensing.

2. Verify that the license has not been removed by another administrator or process in your tenant. You can see a history of license changes made in your tenant on the [Audit logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit) blade.
  You can search for the UPN (for example, <joe@contoso.com>) to see if a license has recently been removed. You can read more about Azure AD audit logs
    [here](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-audit-events).


