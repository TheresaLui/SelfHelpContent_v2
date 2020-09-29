<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_Identifier_Missing"
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
This application has multiple Identifiers (Entity IDs), and no default Identifier has been configured. IDP initiated sign in requires a default identifier to be configured so that the SAML response contains the correct audience.   
<!--/issueDescription-->


## **Recommended Steps**

Configure a default identifier for this application. To do this: 

1. Open the enterprise application in the Azure Portal, and select **Single sign-on**, and then **SAML**   
   
2. Edit the **Basic SAML configuration**
   
3. In the **Identifier (Entity ID) section**, select one of the Identifiers (Entity IDs) to be the default, and save the configuration change

Follow the steps documented [here](https://docs.microsoft.com/azure/active-directory/manage-apps/application-sign-in-problem-federated-sso-gallery#application-not-found-in-directory).
