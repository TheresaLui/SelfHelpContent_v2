<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_Reply_Url_Missing"
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
This application has multiple reply URLs, and no default reply URL has been configured. IDP initiated sign in requires a default URL to be configured so that the SAML response can be sent to the right endpoint.  
<!--/issueDescription-->


## **Recommended Steps**

Configure a default reply URL for this application. To do this: 

1. Open the enterprise application in the Azure Portal, and select **Single sign-on**, and then **SAML**
   
2. Edit the **Basic SAML configuration**
   
3. In the **Reply URL** section, select one of the reply URLs to be the default, and save the configuration change
