<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_75005"
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
Azure AD doesn’t support the SAML request sent by the application for single sign-on. 
<!--/issueDescription-->

Some common issues are: 
  1. Missing required fields in the SAML request 
   
  2. SAML request encoded method 

## **Recommended Steps**

Follow the steps documented [here](https://docs.microsoft.com/azure/active-directory/manage-apps/application-sign-in-problem-federated-sso-gallery#not-a-valid-saml-request).