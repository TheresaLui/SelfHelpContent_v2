<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_Issuer_Attribute_Mismatch"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# Configuration Issue Preventing User Sign-In
<!--issueDescription-->
The Issuer attribute sent from the application to Azure AD in the SAML request doesn’t match the Identifier value that's configured for the application in Azure AD. 
<!--/issueDescription-->

## **Recommended Steps**
Follow the steps documented [here](https://docs.microsoft.com/azure/active-directory/manage-apps/application-sign-in-problem-federated-sso-gallery#application-not-found-in-directory).