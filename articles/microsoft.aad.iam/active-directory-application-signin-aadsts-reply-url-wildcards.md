<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_Reply_Url_Wildcards"
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
The reply URL(s) for this application have wildcards. IDP initiated sign-in requires a reply URL that does not contain wildcards. 
<!--/issueDescription-->


## **Recommended Steps**

Configure a default reply URL for this application. To do this: 

1. Open the enterprise application in the Azure Portal, and select **Single sign-on**, and then **SAML**
   
2. Edit the **Basic SAML configuration**   
   
3. In the **Reply URL** section, edit an existing reply URL or add new URL that does not contain wildcards
   
4. Select that reply URL as the default, and save the configuration change
   
