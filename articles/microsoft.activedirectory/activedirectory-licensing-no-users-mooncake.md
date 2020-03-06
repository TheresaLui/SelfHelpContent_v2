 <properties 
    pageTitle="A user doesn't have the right licenses"
    description="A user doesn't have the right licenses"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    ms.author="piotrci"
    displayOrder="26"
    supportTopicIds=""
    selfHelpType="resource"
    resourceTags="licensing_overview"
    productPesIds=""
    cloudEnvironments="MoonCake"
 	articleId="activedirectory-licensing-no-users-mooncake"
	ownershipId="AzureIdentity_User"
/>

# A user doesn't have the right licenses

## **Recommended Steps**

The full information about user licenses and their status is available on the **Licenses** blade for that user. If you don't see the licenses that you expect, try these tips.

1. Verify that the license has not been removed by another administrator or process in your tenant. You can see a history of license changes made in your tenant on the [Audit logs blade](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit). You can search for the UPN (for example, joe@contoso.com) to see if a license has recently been removed. You can also [read more about Azure AD audit logs](https://docs.azure.cn/active-directory/reports-monitoring/concept-audit-logs).


