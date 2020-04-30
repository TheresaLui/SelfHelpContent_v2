<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_Missing_Redirect_Binding"
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
You are missing HTTP redirect binding in the SAML request to Azure AD.
<!--/issueDescription-->

## **Recommended Steps**
In order to enable user sign-in for this application, please update your application to send the SAML request encoded into the location header using HTTP redirect binding. For more information about how to implement it, read the section HTTP Redirect Binding in the [SAML protocol specification document](https://docs.oasis-open.org/security/saml/v2.0/saml-bindings-2.0-os.pdf).

Your application should now be available for user sign-in.

For future sign in problems with SAML based applications, we recommend using the [testing feature with the My Apps secure sign-in extension](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-debugging) to get better and automatic self diagnosis and resolution steps.

## **Recommended Documents**

* [Problem SignIn gallery applications](https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery)
