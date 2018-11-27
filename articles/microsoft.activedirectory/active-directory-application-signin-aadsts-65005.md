<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_65005"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

The application you were trying to sign into does not exist in the Azure Active Directory. The application may not be configured properly in Azure AD. The Issuer value that is coming in the sign in request (SAML request) does not match the application Identifier.

In order to enable user sign-in for this application, please follow the steps below:

**Step 1**: Identify the value of the “Issuer” property in the SAML request from the application.  Follow the instructions in this document to obtain a SAML request: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->.

**Step 2**: Sign in to the Azure Portal as a global administrator or another role that is able to manage this application.

**Step 3**: Select Azure Active Directory and go to the 'Enterprise applications' blade. Search for the application for which you want to enable federated single sign-on.

**Step 4**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step 5**: Within the 'Basic SAML Configuration' section, select the edit pencil.  Enter the Issuer value into the 'Identifier (Entity ID)' property and select Save.  

Your application should now be available for user sign-in.

For future sign in problems with SAML based applications, we recommend using the testing feature with the My Apps secure sign-in extension to get better and automatic self diagnosis and resolution steps. For more information see: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->
