<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    authoralias="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_With_SAML_Request_65005"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration Issue Preventing User Sign-In

The application you were trying to sign into does not exist in the Azure Active Directory. The application may not be configured properly in Azure AD, or the Issuer value that is coming in the sign-in request (SAML request) does not match the application Identifier.

In order to enable user sign-in for this application, please follow the steps below:

1. Refer to the SAML request provided at the end of this article under the title "SAML Request Received" and copy it
2. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
3. Select **Azure Active Directory** and go the "Enterprise applications" blade. Search for the application for which you want to enable federated single sign-on.
4. Click on the application name to open it, then click "Single Sign-On" on the application's left-hand navigation menu
5. Within the "Basic SAML Configuration' section", click the pencil to edit the value
6. Enter the Issuer value into the "Identifier (Entity ID)" property and click save 

Your application should now be available for user sign-in.
 
For future sign in problems with SAML based applications, we recommend using the testing feature with the My Apps secure sign-in extension to get better and automatic self diagnosis and resolution steps. For more information see: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->

<h4>SAML Request Received:</h4>				
<!--$SAMLRequestFormatted-->SAMLRequestFormatted<!--/$SAMLRequestFormatted-->	
