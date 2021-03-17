<properties
    pageTitle="Admin Consent Issues"
    description="Common issues related to Admin Consent"
    infoBubbleText="Please try self diagnosis with our intelligent knowledge base"
    service="microsoft.activedirectory"
    resource=""
    authors="rachundi"
    ms.author="rachundi"
    displayOrder="1"
    articleId="ml-enterprise-apps-admin-consent"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# Resolving Admin Consent Issues? 

<!--issueDescription-->
Based on the summary problem description, the issue you are encountering could be due to one of the following reasons.
<!--/issueDescription-->

1.	The application wasn't found in the Azure Active Directory tenant. This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant.
2.	The application may not have the permissions needed to perform what the app requested
3.	The user or admin does not have consent for the app to run

## **Recommended Documents**

* [Configure how end-users consent to applications](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-user-consent) 
* [Permissions and consent in the Microsoft identity platform endpoint](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent)

## **Action**

You can click on the link below to directly navigate to Enterprise Applications to review and fix the configuration issue for the application: [Enterprise Applications](https://portal.azure.com/#blade/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/AllApps/menuId/)
