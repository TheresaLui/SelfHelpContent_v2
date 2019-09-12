<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_With_SAML_Request_75005"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration Issue Preventing User Sign-In
<!--issueDescription-->
The authentication/SAML request that you are sending is invalid or missing properties.
<!--issueDescription-->

## **Recommended Steps**

1. Refer to and make note of the SAML request provided at the end of this list under the title **SAML Request Received**
2. Contact the application vendor and share the following info:

    a. SAML Request from above
    b. Azure AD Single SignOn [protocol requirements](https://docs.microsoft.com/azure/active-directory/develop/active-directory-single-sign-on-protocol-reference)

Your application should be available for user sign-in once the authentication request contains the required fields.

For future sign in problems with SAML based applications, we recommend using the [testing feature with the My Apps secure sign-in extension](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-debugging) to get better and automatic self diagnosis and resolution steps.

## **Recommended Documents**

* [Problem SignIn gallery applications](https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery)

### SAML Request Received

<!--$SAMLRequestFormatted-->SAMLRequestFormatted<!--/$SAMLRequestFormatted-->
